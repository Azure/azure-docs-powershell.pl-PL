---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189658"
---
# <span data-ttu-id="74fee-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74fee-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="74fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74fee-102">SYNOPSIS</span></span>
<span data-ttu-id="74fee-103">Tworzy konfigurację reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="74fee-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="74fee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74fee-104">SYNTAX</span></span>

### <span data-ttu-id="74fee-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="74fee-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74fee-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74fee-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74fee-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="74fee-107">DESCRIPTION</span></span>
<span data-ttu-id="74fee-108">Polecenie **cmdlet New-AzNetworkSecurityRuleConfig** tworzy konfigurację reguły zabezpieczeń sieci platformy Azure dla grupy zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="74fee-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="74fee-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74fee-109">EXAMPLES</span></span>

### <span data-ttu-id="74fee-110">Przykład 1. Tworzenie reguły zabezpieczeń sieciowej umożliwiającej dostęp do protokołu RDP</span><span class="sxs-lookup"><span data-stu-id="74fee-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="74fee-111">To polecenie tworzy regułę zabezpieczeń umożliwiającą dostęp z Internetu do portu 3389</span><span class="sxs-lookup"><span data-stu-id="74fee-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="74fee-112">Przykład 2. Tworzenie reguły zabezpieczeń sieci, która zezwala na protokół HTTP</span><span class="sxs-lookup"><span data-stu-id="74fee-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="74fee-113">To polecenie tworzy regułę zabezpieczeń umożliwiającą dostęp z Internetu do portu 80</span><span class="sxs-lookup"><span data-stu-id="74fee-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="74fee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74fee-114">PARAMETERS</span></span>

### <span data-ttu-id="74fee-115">— Access</span><span class="sxs-lookup"><span data-stu-id="74fee-115">-Access</span></span>
<span data-ttu-id="74fee-116">Określa, czy ruch sieciowy jest dozwolony, czy odrzucony.</span><span class="sxs-lookup"><span data-stu-id="74fee-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="74fee-117">Dopuszczalne wartości dla tego parametru to: Allow (Zezwalaj) i Deny (Odmów).</span><span class="sxs-lookup"><span data-stu-id="74fee-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="74fee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fee-118">-DefaultProfile</span></span>
<span data-ttu-id="74fee-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74fee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74fee-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="74fee-120">-Description</span></span>
<span data-ttu-id="74fee-121">Określa opis konfiguracji reguły zabezpieczeń sieci, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="74fee-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="74fee-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="74fee-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="74fee-123">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="74fee-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="74fee-124">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74fee-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74fee-125">Adres routingu międzydomenowego (CIDR, Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="74fee-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="74fee-126">Zakres docelowych adresów IP</span><span class="sxs-lookup"><span data-stu-id="74fee-126">A destination IP address range</span></span> 
- <span data-ttu-id="74fee-127">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP Możesz użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="74fee-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="74fee-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="74fee-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="74fee-129">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="74fee-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="74fee-130">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="74fee-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="74fee-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="74fee-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="74fee-132">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="74fee-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="74fee-133">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="74fee-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="74fee-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="74fee-134">-DestinationPortRange</span></span>
<span data-ttu-id="74fee-135">Określa port lub zakres docelowy.</span><span class="sxs-lookup"><span data-stu-id="74fee-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="74fee-136">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74fee-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74fee-137">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="74fee-137">An integer</span></span>
- <span data-ttu-id="74fee-138">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="74fee-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="74fee-139">Symbol wieloznaczny (\*) do dopasowania dowolnego portu</span><span class="sxs-lookup"><span data-stu-id="74fee-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="74fee-140">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="74fee-140">-Direction</span></span>
<span data-ttu-id="74fee-141">Określa, czy reguła jest szacowana dla ruchu przychodzącego lub wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="74fee-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="74fee-142">Dopuszczalne wartości dla tego parametru to: Przychodzący i wychodzący.</span><span class="sxs-lookup"><span data-stu-id="74fee-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="74fee-143">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74fee-143">-Name</span></span>
<span data-ttu-id="74fee-144">Określa nazwę konfiguracji reguły zabezpieczeń sieciowej, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74fee-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="74fee-145">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="74fee-145">-Priority</span></span>
<span data-ttu-id="74fee-146">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="74fee-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="74fee-147">Dopuszczalne wartości dla tego parametru to: liczba całkowita z między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="74fee-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="74fee-148">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="74fee-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="74fee-149">Im niższy numer priorytetu, tym wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="74fee-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="74fee-150">— Protokół</span><span class="sxs-lookup"><span data-stu-id="74fee-150">-Protocol</span></span>
<span data-ttu-id="74fee-151">Określa protokół sieciowy, do których ma zastosowanie nowa konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="74fee-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="74fee-152">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74fee-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74fee-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="74fee-153">Tcp</span></span>
- <span data-ttu-id="74fee-154">Udp</span><span class="sxs-lookup"><span data-stu-id="74fee-154">Udp</span></span>
- <span data-ttu-id="74fee-155">symbol wieloznaczny (\*), aby dopasować je do obu.</span><span class="sxs-lookup"><span data-stu-id="74fee-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="74fee-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="74fee-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="74fee-157">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="74fee-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="74fee-158">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74fee-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74fee-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="74fee-159">A CIDR</span></span>
- <span data-ttu-id="74fee-160">Źródłowy zakres adresów IP</span><span class="sxs-lookup"><span data-stu-id="74fee-160">A source IP range</span></span>
- <span data-ttu-id="74fee-161">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="74fee-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="74fee-162">Możesz również używać tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="74fee-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="74fee-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="74fee-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="74fee-164">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="74fee-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="74fee-165">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="74fee-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="74fee-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="74fee-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="74fee-167">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="74fee-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="74fee-168">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="74fee-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="74fee-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="74fee-169">-SourcePortRange</span></span>
<span data-ttu-id="74fee-170">Określa port lub zakres źródłowy.</span><span class="sxs-lookup"><span data-stu-id="74fee-170">Specifies the source port or range.</span></span>
<span data-ttu-id="74fee-171">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="74fee-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74fee-172">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="74fee-172">An integer</span></span>
- <span data-ttu-id="74fee-173">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="74fee-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="74fee-174">Symbol wieloznaczny (\*) do dopasowania dowolnego portu</span><span class="sxs-lookup"><span data-stu-id="74fee-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="74fee-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fee-175">CommonParameters</span></span>
<span data-ttu-id="74fee-176">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fee-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fee-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74fee-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fee-178">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74fee-178">INPUTS</span></span>

### <span data-ttu-id="74fee-179">Brak</span><span class="sxs-lookup"><span data-stu-id="74fee-179">None</span></span>

## <span data-ttu-id="74fee-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74fee-180">OUTPUTS</span></span>

### <span data-ttu-id="74fee-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="74fee-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="74fee-182">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74fee-182">NOTES</span></span>

## <span data-ttu-id="74fee-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74fee-183">RELATED LINKS</span></span>

[<span data-ttu-id="74fee-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74fee-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="74fee-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74fee-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="74fee-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74fee-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="74fee-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74fee-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


