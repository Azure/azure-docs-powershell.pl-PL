---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339397"
---
# <span data-ttu-id="fb00c-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb00c-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="fb00c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb00c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb00c-103">Dodaje konfigurację reguły zabezpieczeń sieci do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="fb00c-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="fb00c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb00c-104">SYNTAX</span></span>

### <span data-ttu-id="fb00c-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fb00c-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb00c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb00c-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb00c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fb00c-107">DESCRIPTION</span></span>
<span data-ttu-id="fb00c-108">Polecenie cmdlet **Add-AzNetworkSecurityRuleConfig** umożliwia dodanie konfiguracji reguł zabezpieczeń sieci do grupy zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb00c-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="fb00c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb00c-109">EXAMPLES</span></span>

### <span data-ttu-id="fb00c-110">1: Dodawanie grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="fb00c-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="fb00c-111">Pierwsze polecenie pobiera grupę zabezpieczeń sieci Azure o nazwie "nsg1" z grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="fb00c-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="fb00c-112">Drugie polecenie dodaje regułę zabezpieczeń sieci o nazwie "RDP-Rule", która umożliwia ruch z Internetu na porcie 3389 do pobranego obiektu grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="fb00c-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="fb00c-113">Utrzymuje zmienioną grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="fb00c-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="fb00c-114">2: Dodawanie nowej reguły zabezpieczeń za pomocą grup zabezpieczeń aplikacji</span><span class="sxs-lookup"><span data-stu-id="fb00c-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="fb00c-115">Najpierw tworzymy dwie nowe grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb00c-115">First, we create two new application security groups.</span></span> <span data-ttu-id="fb00c-116">Następnie pobieramy grupę zabezpieczeń sieci Azure o nazwie "nsg1" z grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="fb00c-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="fb00c-117">i Dodaj do niej regułę zabezpieczeń sieci o nazwie "RDP-Rule".</span><span class="sxs-lookup"><span data-stu-id="fb00c-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="fb00c-118">Reguła zezwala na ruch ze wszystkich konfiguracji adresów IP w grupie zabezpieczeń aplikacji "srcAsg" do wszystkich konfiguracji adresów IP w "destAsg" na porcie 3389.</span><span class="sxs-lookup"><span data-stu-id="fb00c-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="fb00c-119">Po dodaniu reguły zachowywana jest Twoja zmieniona Grupa zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="fb00c-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="fb00c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb00c-120">PARAMETERS</span></span>

### <span data-ttu-id="fb00c-121">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="fb00c-121">-Access</span></span>
<span data-ttu-id="fb00c-122">Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="fb00c-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="fb00c-123">Dopuszczalne wartości tego parametru to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="fb00c-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="fb00c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb00c-124">-DefaultProfile</span></span>
<span data-ttu-id="fb00c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb00c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb00c-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="fb00c-126">-Description</span></span>
<span data-ttu-id="fb00c-127">Określa opis konfiguracji reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="fb00c-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="fb00c-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fb00c-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="fb00c-129">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="fb00c-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="fb00c-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fb00c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb00c-131">Adres międzydomenowy (Classless indomain Routing)</span><span class="sxs-lookup"><span data-stu-id="fb00c-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="fb00c-132">Zakres docelowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="fb00c-132">A destination IP address range</span></span>
- <span data-ttu-id="fb00c-133">Symbol wieloznaczny (\*), aby dopasować dowolny adres IP, za pomocą których można korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="fb00c-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="fb00c-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb00c-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="fb00c-135">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="fb00c-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="fb00c-136">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="fb00c-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fb00c-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fb00c-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="fb00c-138">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="fb00c-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="fb00c-139">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="fb00c-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fb00c-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="fb00c-140">-DestinationPortRange</span></span>
<span data-ttu-id="fb00c-141">Określa port docelowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="fb00c-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="fb00c-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fb00c-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb00c-143">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="fb00c-143">An integer</span></span>
- <span data-ttu-id="fb00c-144">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="fb00c-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="fb00c-145">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="fb00c-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="fb00c-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="fb00c-146">-Direction</span></span>
<span data-ttu-id="fb00c-147">Określa, czy reguła jest obliczana na ruch przychodzący lub wychodzący.</span><span class="sxs-lookup"><span data-stu-id="fb00c-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="fb00c-148">Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="fb00c-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="fb00c-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb00c-149">-Name</span></span>
<span data-ttu-id="fb00c-150">Określa nazwę konfiguracji reguł zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="fb00c-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="fb00c-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb00c-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fb00c-152">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="fb00c-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="fb00c-153">To polecenie cmdlet umożliwia dodanie konfiguracji reguły zabezpieczeń sieci do obiektu, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="fb00c-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb00c-154">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="fb00c-154">-Priority</span></span>
<span data-ttu-id="fb00c-155">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="fb00c-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="fb00c-156">Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="fb00c-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="fb00c-157">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="fb00c-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="fb00c-158">Niższy numer priorytetu, wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="fb00c-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="fb00c-159">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="fb00c-159">-Protocol</span></span>
<span data-ttu-id="fb00c-160">Określa protokół sieciowy, którego dotyczy konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="fb00c-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="fb00c-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fb00c-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb00c-162">Protokoł</span><span class="sxs-lookup"><span data-stu-id="fb00c-162">Tcp</span></span>
- <span data-ttu-id="fb00c-163">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="fb00c-163">Udp</span></span>
- <span data-ttu-id="fb00c-164">Symbol wieloznaczny (\*), aby dopasować oba znaki</span><span class="sxs-lookup"><span data-stu-id="fb00c-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="fb00c-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fb00c-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="fb00c-166">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="fb00c-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="fb00c-167">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fb00c-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb00c-168">CIDR</span><span class="sxs-lookup"><span data-stu-id="fb00c-168">A CIDR</span></span>
- <span data-ttu-id="fb00c-169">Zakres źródłowy adresu IP</span><span class="sxs-lookup"><span data-stu-id="fb00c-169">A source IP range</span></span>
- <span data-ttu-id="fb00c-170">Znak wieloznaczny (\*), aby dopasować dowolny adres IP.</span><span class="sxs-lookup"><span data-stu-id="fb00c-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="fb00c-171">Możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="fb00c-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="fb00c-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb00c-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="fb00c-173">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="fb00c-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="fb00c-174">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="fb00c-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fb00c-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fb00c-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="fb00c-176">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="fb00c-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="fb00c-177">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="fb00c-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fb00c-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="fb00c-178">-SourcePortRange</span></span>
<span data-ttu-id="fb00c-179">Określa port źródłowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="fb00c-179">Specifies a source port or range.</span></span>
<span data-ttu-id="fb00c-180">Ta wartość jest wyrażona jako liczba całkowita z zakresu od 0 do 65535 lub jako symbol wieloznaczny (\*) w celu dopasowania dowolnego portu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="fb00c-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="fb00c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb00c-181">CommonParameters</span></span>
<span data-ttu-id="fb00c-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb00c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb00c-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb00c-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb00c-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb00c-184">INPUTS</span></span>

### <span data-ttu-id="fb00c-185">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb00c-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fb00c-186">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb00c-186">OUTPUTS</span></span>

### <span data-ttu-id="fb00c-187">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb00c-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fb00c-188">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb00c-188">NOTES</span></span>

## <span data-ttu-id="fb00c-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb00c-189">RELATED LINKS</span></span>

[<span data-ttu-id="fb00c-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb00c-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fb00c-191">Nowe — AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb00c-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fb00c-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb00c-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fb00c-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb00c-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


