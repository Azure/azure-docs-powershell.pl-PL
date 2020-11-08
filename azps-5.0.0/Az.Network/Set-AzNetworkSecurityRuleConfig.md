---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225702"
---
# <span data-ttu-id="58a75-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58a75-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="58a75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58a75-102">SYNOPSIS</span></span>
<span data-ttu-id="58a75-103">Aktualizuje konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="58a75-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="58a75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58a75-104">SYNTAX</span></span>

### <span data-ttu-id="58a75-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58a75-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a75-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58a75-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58a75-107">Opis</span><span class="sxs-lookup"><span data-stu-id="58a75-107">DESCRIPTION</span></span>
<span data-ttu-id="58a75-108">Polecenie cmdlet **Set-AzNetworkSecurityRuleConfig** aktualizuje konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="58a75-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="58a75-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58a75-109">EXAMPLES</span></span>

### <span data-ttu-id="58a75-110">Przykład 1. Zmienianie konfiguracji dostępu w regule zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="58a75-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="58a75-111">Pierwsze polecenie uzyskuje grupę zabezpieczeń sieci o nazwie NSG-fronton, a następnie zapisuje ją w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="58a75-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="58a75-112">Drugie polecenie używa operatora potoku w celu przekazania grupy zabezpieczeń w $nsg do polecenia Get-AzNetworkSecurityRuleConfig, który uzyskuje konfigurację reguł zabezpieczeń o nazwie RDP-rule.</span><span class="sxs-lookup"><span data-stu-id="58a75-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="58a75-113">W trzecim poleceniu jest zmieniana Konfiguracja dostępu protokołu RDP — reguła jest odrzucana.</span><span class="sxs-lookup"><span data-stu-id="58a75-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="58a75-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58a75-114">Example 2</span></span>

<span data-ttu-id="58a75-115">Aktualizuje konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="58a75-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="58a75-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="58a75-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="58a75-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58a75-117">PARAMETERS</span></span>

### <span data-ttu-id="58a75-118">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="58a75-118">-Access</span></span>
<span data-ttu-id="58a75-119">Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="58a75-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="58a75-120">Dopuszczalne wartości tego parametru to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="58a75-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="58a75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a75-121">-DefaultProfile</span></span>
<span data-ttu-id="58a75-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58a75-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58a75-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="58a75-123">-Description</span></span>
<span data-ttu-id="58a75-124">Umożliwia określenie opisu konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="58a75-125">Maksymalny rozmiar to 140 znaków.</span><span class="sxs-lookup"><span data-stu-id="58a75-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="58a75-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="58a75-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="58a75-127">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="58a75-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="58a75-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58a75-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58a75-129">Adres międzydomenowy (Classless indomain Routing)</span><span class="sxs-lookup"><span data-stu-id="58a75-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="58a75-130">Zakres docelowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="58a75-130">A destination IP address range</span></span> 
- <span data-ttu-id="58a75-131">Symbol wieloznaczny (\*), aby dopasować dowolny adres IP, za pomocą których można korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="58a75-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="58a75-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58a75-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="58a75-133">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="58a75-134">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="58a75-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="58a75-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="58a75-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="58a75-136">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="58a75-137">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="58a75-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="58a75-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="58a75-138">-DestinationPortRange</span></span>
<span data-ttu-id="58a75-139">Określa port docelowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="58a75-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="58a75-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58a75-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58a75-141">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="58a75-141">An integer</span></span> 
- <span data-ttu-id="58a75-142">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="58a75-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="58a75-143">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="58a75-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="58a75-144">-Direction</span><span class="sxs-lookup"><span data-stu-id="58a75-144">-Direction</span></span>
<span data-ttu-id="58a75-145">Określa, czy reguła jest obliczana na potrzeby ruchu przychodzącego lub wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="58a75-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="58a75-146">Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="58a75-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="58a75-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58a75-147">-Name</span></span>
<span data-ttu-id="58a75-148">Określa nazwę konfiguracji reguł zabezpieczeń sieci, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58a75-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="58a75-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58a75-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="58a75-150">Określa obiekt **NetworkSecurityGroup** , który zawiera konfigurację reguł zabezpieczeń sieci do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="58a75-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="58a75-151">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="58a75-151">-Priority</span></span>
<span data-ttu-id="58a75-152">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="58a75-153">Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="58a75-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="58a75-154">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="58a75-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="58a75-155">Niższy numer priorytetu, wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="58a75-156">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="58a75-156">-Protocol</span></span>
<span data-ttu-id="58a75-157">Określa protokół sieciowy, którego dotyczy konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="58a75-158">Dopuszczalne wartości tego parametru to:--TCP</span><span class="sxs-lookup"><span data-stu-id="58a75-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="58a75-159">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="58a75-159">Udp</span></span>
- <span data-ttu-id="58a75-160">Znak wieloznaczny (\*) zgodny z obydwoma</span><span class="sxs-lookup"><span data-stu-id="58a75-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="58a75-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="58a75-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="58a75-162">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="58a75-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="58a75-163">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58a75-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58a75-164">CIDR</span><span class="sxs-lookup"><span data-stu-id="58a75-164">A CIDR</span></span>
- <span data-ttu-id="58a75-165">Zakres źródłowy adresu IP</span><span class="sxs-lookup"><span data-stu-id="58a75-165">A source IP range</span></span>
- <span data-ttu-id="58a75-166">Symbol wieloznaczny (\*), aby dopasować dowolny adres IP, możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="58a75-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="58a75-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58a75-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="58a75-168">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="58a75-169">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="58a75-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="58a75-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="58a75-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="58a75-171">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="58a75-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="58a75-172">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="58a75-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="58a75-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="58a75-173">-SourcePortRange</span></span>
<span data-ttu-id="58a75-174">Określa port źródłowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="58a75-174">Specifies the source port or range.</span></span>
<span data-ttu-id="58a75-175">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58a75-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58a75-176">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="58a75-176">An integer</span></span>
- <span data-ttu-id="58a75-177">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="58a75-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="58a75-178">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="58a75-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="58a75-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a75-179">CommonParameters</span></span>
<span data-ttu-id="58a75-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a75-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a75-181">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a75-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a75-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58a75-182">INPUTS</span></span>

### <span data-ttu-id="58a75-183">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58a75-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="58a75-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58a75-184">OUTPUTS</span></span>

### <span data-ttu-id="58a75-185">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58a75-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="58a75-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58a75-186">NOTES</span></span>

## <span data-ttu-id="58a75-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58a75-187">RELATED LINKS</span></span>

[<span data-ttu-id="58a75-188">Dodaj-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58a75-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="58a75-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58a75-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="58a75-190">Nowe — AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58a75-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="58a75-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58a75-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


