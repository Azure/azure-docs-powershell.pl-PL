---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708954"
---
# <span data-ttu-id="b530b-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b530b-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b530b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b530b-102">SYNOPSIS</span></span>
<span data-ttu-id="b530b-103">Aktualizuje konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b530b-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="b530b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b530b-104">SYNTAX</span></span>

### <span data-ttu-id="b530b-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b530b-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b530b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b530b-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b530b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b530b-107">DESCRIPTION</span></span>
<span data-ttu-id="b530b-108">Polecenie cmdlet **Set-AzNetworkSecurityRuleConfig** aktualizuje konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b530b-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="b530b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b530b-109">EXAMPLES</span></span>

### <span data-ttu-id="b530b-110">Przykład 1. Zmienianie konfiguracji dostępu w regule zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="b530b-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="b530b-111">Pierwsze polecenie uzyskuje grupę zabezpieczeń sieci o nazwie NSG-fronton, a następnie zapisuje ją w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="b530b-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="b530b-112">Drugie polecenie używa operatora potoku w celu przekazania grupy zabezpieczeń w $nsg do polecenia Get-AzNetworkSecurityRuleConfig, który uzyskuje konfigurację reguł zabezpieczeń o nazwie RDP-rule.</span><span class="sxs-lookup"><span data-stu-id="b530b-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="b530b-113">W trzecim poleceniu jest zmieniana Konfiguracja dostępu protokołu RDP — reguła jest odrzucana.</span><span class="sxs-lookup"><span data-stu-id="b530b-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="b530b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b530b-114">PARAMETERS</span></span>

### <span data-ttu-id="b530b-115">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="b530b-115">-Access</span></span>
<span data-ttu-id="b530b-116">Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="b530b-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="b530b-117">Dopuszczalne wartości tego parametru to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="b530b-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="b530b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b530b-118">-DefaultProfile</span></span>
<span data-ttu-id="b530b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b530b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b530b-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="b530b-120">-Description</span></span>
<span data-ttu-id="b530b-121">Umożliwia określenie opisu konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="b530b-122">Maksymalny rozmiar to 140 znaków.</span><span class="sxs-lookup"><span data-stu-id="b530b-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="b530b-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b530b-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="b530b-124">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="b530b-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="b530b-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b530b-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b530b-126">Adres międzydomenowy (Classless indomain Routing)</span><span class="sxs-lookup"><span data-stu-id="b530b-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="b530b-127">Zakres docelowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="b530b-127">A destination IP address range</span></span> 
- <span data-ttu-id="b530b-128">Symbol wieloznaczny (\*), aby dopasować dowolny adres IP, za pomocą których można korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="b530b-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="b530b-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b530b-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="b530b-130">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b530b-131">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b530b-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b530b-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b530b-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="b530b-133">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b530b-134">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b530b-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b530b-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="b530b-135">-DestinationPortRange</span></span>
<span data-ttu-id="b530b-136">Określa port docelowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="b530b-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="b530b-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b530b-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b530b-138">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="b530b-138">An integer</span></span> 
- <span data-ttu-id="b530b-139">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="b530b-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b530b-140">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="b530b-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b530b-141">-Direction</span><span class="sxs-lookup"><span data-stu-id="b530b-141">-Direction</span></span>
<span data-ttu-id="b530b-142">Określa, czy reguła jest obliczana na potrzeby ruchu przychodzącego lub wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="b530b-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="b530b-143">Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="b530b-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="b530b-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b530b-144">-Name</span></span>
<span data-ttu-id="b530b-145">Określa nazwę konfiguracji reguł zabezpieczeń sieci, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b530b-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b530b-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b530b-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b530b-147">Określa obiekt **NetworkSecurityGroup** , który zawiera konfigurację reguł zabezpieczeń sieci do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="b530b-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b530b-148">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="b530b-148">-Priority</span></span>
<span data-ttu-id="b530b-149">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="b530b-150">Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="b530b-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="b530b-151">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b530b-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="b530b-152">Niższy numer priorytetu, wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="b530b-153">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b530b-153">-Protocol</span></span>
<span data-ttu-id="b530b-154">Określa protokół sieciowy, którego dotyczy konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="b530b-155">Dopuszczalne wartości tego parametru to:--TCP</span><span class="sxs-lookup"><span data-stu-id="b530b-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="b530b-156">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="b530b-156">Udp</span></span>
- <span data-ttu-id="b530b-157">Znak wieloznaczny (\*) zgodny z obydwoma</span><span class="sxs-lookup"><span data-stu-id="b530b-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="b530b-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b530b-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="b530b-159">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="b530b-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="b530b-160">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b530b-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b530b-161">CIDR</span><span class="sxs-lookup"><span data-stu-id="b530b-161">A CIDR</span></span>
- <span data-ttu-id="b530b-162">Zakres źródłowy adresu IP</span><span class="sxs-lookup"><span data-stu-id="b530b-162">A source IP range</span></span>
- <span data-ttu-id="b530b-163">Symbol wieloznaczny (\*), aby dopasować dowolny adres IP, możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="b530b-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="b530b-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b530b-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="b530b-165">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="b530b-166">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b530b-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b530b-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b530b-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="b530b-168">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="b530b-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="b530b-169">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b530b-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b530b-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="b530b-170">-SourcePortRange</span></span>
<span data-ttu-id="b530b-171">Określa port źródłowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="b530b-171">Specifies the source port or range.</span></span>
<span data-ttu-id="b530b-172">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b530b-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b530b-173">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="b530b-173">An integer</span></span>
- <span data-ttu-id="b530b-174">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="b530b-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b530b-175">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="b530b-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b530b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b530b-176">CommonParameters</span></span>
<span data-ttu-id="b530b-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b530b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b530b-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b530b-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b530b-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b530b-179">INPUTS</span></span>

### <span data-ttu-id="b530b-180">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b530b-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b530b-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b530b-181">OUTPUTS</span></span>

### <span data-ttu-id="b530b-182">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b530b-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b530b-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b530b-183">NOTES</span></span>

## <span data-ttu-id="b530b-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b530b-184">RELATED LINKS</span></span>

[<span data-ttu-id="b530b-185">Dodaj-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b530b-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b530b-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b530b-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b530b-187">Nowe — AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b530b-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b530b-188">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b530b-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


