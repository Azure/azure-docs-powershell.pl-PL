---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192026"
---
# <span data-ttu-id="c6db1-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6db1-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c6db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6db1-102">SYNOPSIS</span></span>
<span data-ttu-id="c6db1-103">Dodaje konfigurację reguły zabezpieczeń sieciowych do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="c6db1-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="c6db1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6db1-104">SYNTAX</span></span>

### <span data-ttu-id="c6db1-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="c6db1-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6db1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6db1-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6db1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6db1-107">DESCRIPTION</span></span>
<span data-ttu-id="c6db1-108">Polecenie **cmdlet Add-AzNetworkSecurityRuleConfig** dodaje konfigurację reguły zabezpieczeń sieci do grupy zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6db1-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="c6db1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6db1-109">EXAMPLES</span></span>

### <span data-ttu-id="c6db1-110">1. Dodawanie grupy zabezpieczeń sieciowych</span><span class="sxs-lookup"><span data-stu-id="c6db1-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="c6db1-111">Pierwsze polecenie pobiera grupę zabezpieczeń sieci azure o nazwie "nsg1" z grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="c6db1-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="c6db1-112">Drugie polecenie dodaje regułę zabezpieczeń sieci o nazwie "reguła rdp", która zezwala na ruch z Internetu na porcie 3389 do obiektu pobranej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="c6db1-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="c6db1-113">Zachowywa zmodyfikowaną grupę zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6db1-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="c6db1-114">2. Dodawanie nowej reguły zabezpieczeń za pomocą grup zabezpieczeń aplikacji</span><span class="sxs-lookup"><span data-stu-id="c6db1-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="c6db1-115">Najpierw tworzymy dwie nowe grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c6db1-115">First, we create two new application security groups.</span></span> <span data-ttu-id="c6db1-116">Następnie pobieramy grupę zabezpieczeń sieci azure o nazwie "nsg1" z grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="c6db1-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="c6db1-117">i dodaj do tej reguły regułę zabezpieczeń sieciową o nazwie "reguła rdp".</span><span class="sxs-lookup"><span data-stu-id="c6db1-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="c6db1-118">Ta reguła zezwala na ruch ze wszystkich konfiguracji adresów IP w grupie zabezpieczeń aplikacji "srcAsg" do wszystkich konfiguracji adresów IP w "destAsg" na porcie 3389.</span><span class="sxs-lookup"><span data-stu-id="c6db1-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="c6db1-119">Po dodaniu reguły zachowywana jest zmodyfikowana grupa zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6db1-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="c6db1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6db1-120">PARAMETERS</span></span>

### <span data-ttu-id="c6db1-121">— Access</span><span class="sxs-lookup"><span data-stu-id="c6db1-121">-Access</span></span>
<span data-ttu-id="c6db1-122">Określa, czy ruch sieciowy jest dozwolony, czy odrzucony.</span><span class="sxs-lookup"><span data-stu-id="c6db1-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="c6db1-123">Dopuszczalne wartości dla tego parametru to: Allow (Zezwalaj) i Deny (Odmów).</span><span class="sxs-lookup"><span data-stu-id="c6db1-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="c6db1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6db1-124">-DefaultProfile</span></span>
<span data-ttu-id="c6db1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6db1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6db1-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="c6db1-126">-Description</span></span>
<span data-ttu-id="c6db1-127">Określa opis konfiguracji reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="c6db1-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="c6db1-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c6db1-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="c6db1-129">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="c6db1-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="c6db1-130">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c6db1-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6db1-131">Adres routingu międzydomenowego (CIDR, Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="c6db1-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="c6db1-132">Zakres docelowych adresów IP</span><span class="sxs-lookup"><span data-stu-id="c6db1-132">A destination IP address range</span></span>
- <span data-ttu-id="c6db1-133">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP Możesz użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="c6db1-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="c6db1-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6db1-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="c6db1-135">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="c6db1-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c6db1-136">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c6db1-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c6db1-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c6db1-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="c6db1-138">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="c6db1-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c6db1-139">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c6db1-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c6db1-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="c6db1-140">-DestinationPortRange</span></span>
<span data-ttu-id="c6db1-141">Określa port lub zakres docelowy.</span><span class="sxs-lookup"><span data-stu-id="c6db1-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="c6db1-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c6db1-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6db1-143">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="c6db1-143">An integer</span></span>
- <span data-ttu-id="c6db1-144">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="c6db1-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="c6db1-145">Symbol wieloznaczny (\*) do dopasowania dowolnego portu</span><span class="sxs-lookup"><span data-stu-id="c6db1-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="c6db1-146">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="c6db1-146">-Direction</span></span>
<span data-ttu-id="c6db1-147">Określa, czy reguła jest szacowana dla ruchu przychodzącego lub wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="c6db1-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="c6db1-148">Dopuszczalne wartości dla tego parametru to: Przychodzący i Wychodzący.</span><span class="sxs-lookup"><span data-stu-id="c6db1-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="c6db1-149">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c6db1-149">-Name</span></span>
<span data-ttu-id="c6db1-150">Określa nazwę konfiguracji reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="c6db1-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="c6db1-151">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6db1-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c6db1-152">Określa obiekt **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="c6db1-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="c6db1-153">To polecenie cmdlet dodaje konfigurację reguły zabezpieczeń sieci do obiektu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c6db1-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6db1-154">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="c6db1-154">-Priority</span></span>
<span data-ttu-id="c6db1-155">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="c6db1-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="c6db1-156">Dopuszczalne wartości dla tego parametru to: Liczba całkowita z między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="c6db1-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="c6db1-157">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="c6db1-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="c6db1-158">Im niższy numer priorytetu, tym wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="c6db1-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="c6db1-159">— Protokół</span><span class="sxs-lookup"><span data-stu-id="c6db1-159">-Protocol</span></span>
<span data-ttu-id="c6db1-160">Określa protokół sieciowy, do których ma zastosowanie konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="c6db1-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="c6db1-161">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c6db1-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6db1-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="c6db1-162">Tcp</span></span>
- <span data-ttu-id="c6db1-163">Udp</span><span class="sxs-lookup"><span data-stu-id="c6db1-163">Udp</span></span>
- <span data-ttu-id="c6db1-164">Symbol wieloznaczny (\*) do dopasowania obu</span><span class="sxs-lookup"><span data-stu-id="c6db1-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="c6db1-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c6db1-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="c6db1-166">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="c6db1-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="c6db1-167">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c6db1-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6db1-168">A CIDR</span><span class="sxs-lookup"><span data-stu-id="c6db1-168">A CIDR</span></span>
- <span data-ttu-id="c6db1-169">Źródłowy zakres adresów IP</span><span class="sxs-lookup"><span data-stu-id="c6db1-169">A source IP range</span></span>
- <span data-ttu-id="c6db1-170">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="c6db1-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="c6db1-171">Możesz również używać tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="c6db1-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="c6db1-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6db1-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="c6db1-173">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="c6db1-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="c6db1-174">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c6db1-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c6db1-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c6db1-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="c6db1-176">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="c6db1-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="c6db1-177">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c6db1-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c6db1-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="c6db1-178">-SourcePortRange</span></span>
<span data-ttu-id="c6db1-179">Określa port lub zakres źródłowy.</span><span class="sxs-lookup"><span data-stu-id="c6db1-179">Specifies a source port or range.</span></span>
<span data-ttu-id="c6db1-180">Ta wartość jest wyrażana jako liczba całkowita, w zakresie od 0 do 65535 lub jako symbol wieloznaczny (\*) w celu dopasowania do dowolnego portu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="c6db1-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="c6db1-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6db1-181">CommonParameters</span></span>
<span data-ttu-id="c6db1-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6db1-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6db1-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6db1-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6db1-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6db1-184">INPUTS</span></span>

### <span data-ttu-id="c6db1-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6db1-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c6db1-186">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6db1-186">OUTPUTS</span></span>

### <span data-ttu-id="c6db1-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6db1-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c6db1-188">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6db1-188">NOTES</span></span>

## <span data-ttu-id="c6db1-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6db1-189">RELATED LINKS</span></span>

[<span data-ttu-id="c6db1-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6db1-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c6db1-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6db1-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c6db1-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6db1-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c6db1-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6db1-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


