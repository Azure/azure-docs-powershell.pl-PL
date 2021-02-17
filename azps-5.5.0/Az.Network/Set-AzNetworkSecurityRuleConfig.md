---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202452"
---
# <span data-ttu-id="03200-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03200-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="03200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03200-102">SYNOPSIS</span></span>
<span data-ttu-id="03200-103">Aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="03200-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="03200-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03200-104">SYNTAX</span></span>

### <span data-ttu-id="03200-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="03200-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03200-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="03200-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03200-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="03200-107">DESCRIPTION</span></span>
<span data-ttu-id="03200-108">Polecenie **cmdlet Set-AzNetworkSecurityRuleConfig** aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="03200-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="03200-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03200-109">EXAMPLES</span></span>

### <span data-ttu-id="03200-110">Przykład 1. Zmienianie konfiguracji dostępu w regułę zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="03200-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="03200-111">Pierwsze polecenie pobiera grupę zabezpieczeń sieci o nazwie NSG-FrontEnd, a następnie przechowuje ją w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="03200-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="03200-112">Drugie polecenie przekaże grupę zabezpieczeń w programie $nsg do usługi Get-AzNetworkSecurityRuleConfig, która pobiera konfigurację reguł zabezpieczeń o nazwie rdp-rule.</span><span class="sxs-lookup"><span data-stu-id="03200-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="03200-113">Trzecie polecenie zmienia konfigurację dostępu reguły rdp na Odmów.</span><span class="sxs-lookup"><span data-stu-id="03200-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="03200-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="03200-114">Example 2</span></span>

<span data-ttu-id="03200-115">Aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="03200-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="03200-116">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="03200-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="03200-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03200-117">PARAMETERS</span></span>

### <span data-ttu-id="03200-118">— Access</span><span class="sxs-lookup"><span data-stu-id="03200-118">-Access</span></span>
<span data-ttu-id="03200-119">Określa, czy ruch sieciowy jest dozwolony, czy odrzucony.</span><span class="sxs-lookup"><span data-stu-id="03200-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="03200-120">Dopuszczalne wartości dla tego parametru to: Allow (Zezwalaj) i Deny (Odmów).</span><span class="sxs-lookup"><span data-stu-id="03200-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="03200-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03200-121">-DefaultProfile</span></span>
<span data-ttu-id="03200-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03200-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03200-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="03200-123">-Description</span></span>
<span data-ttu-id="03200-124">Określa opis konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="03200-125">Maksymalny rozmiar to 140 znaków.</span><span class="sxs-lookup"><span data-stu-id="03200-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="03200-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="03200-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="03200-127">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="03200-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="03200-128">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="03200-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03200-129">Adres routingu międzydomenowego (CIDR, Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="03200-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="03200-130">Zakres docelowych adresów IP</span><span class="sxs-lookup"><span data-stu-id="03200-130">A destination IP address range</span></span> 
- <span data-ttu-id="03200-131">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP Możesz użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="03200-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="03200-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03200-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="03200-133">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="03200-134">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="03200-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="03200-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="03200-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="03200-136">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="03200-137">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="03200-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="03200-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="03200-138">-DestinationPortRange</span></span>
<span data-ttu-id="03200-139">Określa port lub zakres docelowy.</span><span class="sxs-lookup"><span data-stu-id="03200-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="03200-140">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="03200-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03200-141">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="03200-141">An integer</span></span> 
- <span data-ttu-id="03200-142">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="03200-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="03200-143">Symbol wieloznaczny (\*) w celu dopasowania dowolnego portu</span><span class="sxs-lookup"><span data-stu-id="03200-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="03200-144">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="03200-144">-Direction</span></span>
<span data-ttu-id="03200-145">Określa, czy reguła jest szacowana dla ruchu przychodzącego lub wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="03200-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="03200-146">Dopuszczalne wartości dla tego parametru to: Przychodzący i Wychodzący.</span><span class="sxs-lookup"><span data-stu-id="03200-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="03200-147">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03200-147">-Name</span></span>
<span data-ttu-id="03200-148">Określa nazwę konfiguracji reguły zabezpieczeń sieciowych ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03200-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="03200-149">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03200-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="03200-150">Określa obiekt **NetworkSecurityGroup** zawierający konfigurację reguły zabezpieczeń sieci, która ma być ustawiona.</span><span class="sxs-lookup"><span data-stu-id="03200-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="03200-151">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="03200-151">-Priority</span></span>
<span data-ttu-id="03200-152">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="03200-153">Dopuszczalne wartości dla tego parametru to:Liczba całkowita z między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="03200-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="03200-154">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="03200-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="03200-155">Im niższy numer priorytetu, tym wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="03200-156">— Protokół</span><span class="sxs-lookup"><span data-stu-id="03200-156">-Protocol</span></span>
<span data-ttu-id="03200-157">Określa protokół sieciowy, do których ma zastosowanie konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="03200-158">Dopuszczalne wartości dla tego parametru to: --Tcp</span><span class="sxs-lookup"><span data-stu-id="03200-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="03200-159">Udp</span><span class="sxs-lookup"><span data-stu-id="03200-159">Udp</span></span>
- <span data-ttu-id="03200-160">Symbol wieloznaczny (\*) do dopasowania obu</span><span class="sxs-lookup"><span data-stu-id="03200-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="03200-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="03200-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="03200-162">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="03200-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="03200-163">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="03200-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03200-164">A CIDR</span><span class="sxs-lookup"><span data-stu-id="03200-164">A CIDR</span></span>
- <span data-ttu-id="03200-165">Źródłowy zakres adresów IP</span><span class="sxs-lookup"><span data-stu-id="03200-165">A source IP range</span></span>
- <span data-ttu-id="03200-166">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP Możesz również użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="03200-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="03200-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03200-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="03200-168">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="03200-169">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="03200-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="03200-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="03200-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="03200-171">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="03200-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="03200-172">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="03200-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="03200-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="03200-173">-SourcePortRange</span></span>
<span data-ttu-id="03200-174">Określa port lub zakres źródłowy.</span><span class="sxs-lookup"><span data-stu-id="03200-174">Specifies the source port or range.</span></span>
<span data-ttu-id="03200-175">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="03200-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03200-176">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="03200-176">An integer</span></span>
- <span data-ttu-id="03200-177">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="03200-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="03200-178">Symbol wieloznaczny (\*) w celu dopasowania dowolnego portu</span><span class="sxs-lookup"><span data-stu-id="03200-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="03200-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03200-179">CommonParameters</span></span>
<span data-ttu-id="03200-180">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03200-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03200-181">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03200-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03200-182">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03200-182">INPUTS</span></span>

### <span data-ttu-id="03200-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03200-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="03200-184">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03200-184">OUTPUTS</span></span>

### <span data-ttu-id="03200-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03200-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="03200-186">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03200-186">NOTES</span></span>

## <span data-ttu-id="03200-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03200-187">RELATED LINKS</span></span>

[<span data-ttu-id="03200-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03200-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="03200-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03200-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="03200-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03200-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="03200-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="03200-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


