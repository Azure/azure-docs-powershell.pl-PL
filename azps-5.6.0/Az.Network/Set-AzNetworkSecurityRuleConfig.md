---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003274"
---
# <span data-ttu-id="4e340-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e340-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="4e340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e340-102">SYNOPSIS</span></span>
<span data-ttu-id="4e340-103">Aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="4e340-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="4e340-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e340-104">SYNTAX</span></span>

### <span data-ttu-id="4e340-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4e340-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e340-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e340-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e340-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e340-107">DESCRIPTION</span></span>
<span data-ttu-id="4e340-108">Polecenie **cmdlet Set-AzNetworkSecurityRuleConfig** aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="4e340-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="4e340-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e340-109">EXAMPLES</span></span>

### <span data-ttu-id="4e340-110">Przykład 1. Zmienianie konfiguracji dostępu w regułę zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="4e340-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="4e340-111">Pierwsze polecenie pobiera grupę zabezpieczeń sieci o nazwie NSG-FrontEnd, a następnie przechowuje ją w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="4e340-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="4e340-112">Drugie polecenie przekaże grupę zabezpieczeń w programie $nsg do strony Get-AzNetworkSecurityRuleConfig, która pobiera konfigurację reguł zabezpieczeń o nazwie rdp-rule.</span><span class="sxs-lookup"><span data-stu-id="4e340-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="4e340-113">Trzecie polecenie zmienia konfigurację dostępu reguły rdp na Odmów.</span><span class="sxs-lookup"><span data-stu-id="4e340-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="4e340-114">Spowoduje to jednak zastąpienie reguły i ustawienie tylko parametrów przekazywanych do Set-AzNetworkSecurityRuleConfig sieci.</span><span class="sxs-lookup"><span data-stu-id="4e340-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="4e340-115">UWAGA: Nie można zmienić pojedynczego atrybutu</span><span class="sxs-lookup"><span data-stu-id="4e340-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="4e340-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4e340-116">Example 2</span></span>

<span data-ttu-id="4e340-117">Aktualizuje konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="4e340-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="4e340-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="4e340-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="4e340-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e340-119">PARAMETERS</span></span>

### <span data-ttu-id="4e340-120">— Access</span><span class="sxs-lookup"><span data-stu-id="4e340-120">-Access</span></span>
<span data-ttu-id="4e340-121">Określa, czy ruch sieciowy jest dozwolony, czy odrzucony.</span><span class="sxs-lookup"><span data-stu-id="4e340-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="4e340-122">Dopuszczalne wartości dla tego parametru to: Allow (Zezwalaj) i Deny (Odmów).</span><span class="sxs-lookup"><span data-stu-id="4e340-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="4e340-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e340-123">-DefaultProfile</span></span>
<span data-ttu-id="4e340-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e340-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e340-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="4e340-125">-Description</span></span>
<span data-ttu-id="4e340-126">Określa opis konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="4e340-127">Maksymalny rozmiar to 140 znaków.</span><span class="sxs-lookup"><span data-stu-id="4e340-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="4e340-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4e340-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="4e340-129">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="4e340-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="4e340-130">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e340-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e340-131">Adres routingu międzydomenowego (CIDR, Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="4e340-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="4e340-132">Zakres docelowych adresów IP</span><span class="sxs-lookup"><span data-stu-id="4e340-132">A destination IP address range</span></span> 
- <span data-ttu-id="4e340-133">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP Możesz użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="4e340-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="4e340-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e340-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="4e340-135">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4e340-136">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4e340-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4e340-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4e340-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="4e340-138">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4e340-139">Nie można jej używać z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4e340-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4e340-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="4e340-140">-DestinationPortRange</span></span>
<span data-ttu-id="4e340-141">Określa port lub zakres docelowy.</span><span class="sxs-lookup"><span data-stu-id="4e340-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="4e340-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e340-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e340-143">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="4e340-143">An integer</span></span> 
- <span data-ttu-id="4e340-144">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="4e340-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4e340-145">Symbol wieloznaczny (\*) do dopasowania dowolnego portu</span><span class="sxs-lookup"><span data-stu-id="4e340-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4e340-146">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="4e340-146">-Direction</span></span>
<span data-ttu-id="4e340-147">Określa, czy reguła jest szacowana dla ruchu przychodzącego lub wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="4e340-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="4e340-148">Dopuszczalne wartości dla tego parametru to: Przychodzący i wychodzący.</span><span class="sxs-lookup"><span data-stu-id="4e340-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="4e340-149">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4e340-149">-Name</span></span>
<span data-ttu-id="4e340-150">Określa nazwę konfiguracji reguły zabezpieczeń sieciowych ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e340-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4e340-151">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e340-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4e340-152">Określa obiekt **NetworkSecurityGroup** zawierający konfigurację reguły zabezpieczeń sieci, która ma być ustawiona.</span><span class="sxs-lookup"><span data-stu-id="4e340-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="4e340-153">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="4e340-153">-Priority</span></span>
<span data-ttu-id="4e340-154">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="4e340-155">Dopuszczalne wartości dla tego parametru to:Liczba całkowita z między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="4e340-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="4e340-156">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="4e340-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="4e340-157">Im niższy numer priorytetu, tym wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="4e340-158">— Protokół</span><span class="sxs-lookup"><span data-stu-id="4e340-158">-Protocol</span></span>
<span data-ttu-id="4e340-159">Określa protokół sieciowy, do których ma zastosowanie konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="4e340-160">Dopuszczalne wartości dla tego parametru to: --Tcp</span><span class="sxs-lookup"><span data-stu-id="4e340-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="4e340-161">Udp</span><span class="sxs-lookup"><span data-stu-id="4e340-161">Udp</span></span>
- <span data-ttu-id="4e340-162">Symbol wieloznaczny (\*) do dopasowania obu</span><span class="sxs-lookup"><span data-stu-id="4e340-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="4e340-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4e340-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="4e340-164">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="4e340-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="4e340-165">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e340-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e340-166">A CIDR</span><span class="sxs-lookup"><span data-stu-id="4e340-166">A CIDR</span></span>
- <span data-ttu-id="4e340-167">Źródłowy zakres adresów IP</span><span class="sxs-lookup"><span data-stu-id="4e340-167">A source IP range</span></span>
- <span data-ttu-id="4e340-168">Symbol wieloznaczny (\*) do dopasowania dowolnego adresu IP Możesz również użyć tagów, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="4e340-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="4e340-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e340-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="4e340-170">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="4e340-171">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4e340-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4e340-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4e340-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="4e340-173">Grupa zabezpieczeń aplikacji ustawiona jako źródło reguły.</span><span class="sxs-lookup"><span data-stu-id="4e340-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="4e340-174">Nie można jej używać z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4e340-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4e340-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="4e340-175">-SourcePortRange</span></span>
<span data-ttu-id="4e340-176">Określa port lub zakres źródłowy.</span><span class="sxs-lookup"><span data-stu-id="4e340-176">Specifies the source port or range.</span></span>
<span data-ttu-id="4e340-177">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e340-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e340-178">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="4e340-178">An integer</span></span>
- <span data-ttu-id="4e340-179">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="4e340-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4e340-180">Symbol wieloznaczny (\*) do dopasowania dowolnego portu</span><span class="sxs-lookup"><span data-stu-id="4e340-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4e340-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e340-181">CommonParameters</span></span>
<span data-ttu-id="4e340-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e340-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e340-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e340-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e340-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e340-184">INPUTS</span></span>

### <span data-ttu-id="4e340-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e340-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4e340-186">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e340-186">OUTPUTS</span></span>

### <span data-ttu-id="4e340-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4e340-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4e340-188">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e340-188">NOTES</span></span>

## <span data-ttu-id="4e340-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e340-189">RELATED LINKS</span></span>

[<span data-ttu-id="4e340-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e340-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4e340-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e340-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4e340-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e340-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4e340-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e340-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


