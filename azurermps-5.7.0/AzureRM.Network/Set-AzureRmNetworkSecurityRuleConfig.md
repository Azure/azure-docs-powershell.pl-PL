---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: c1febd5d39e99ef52e940c590fcd43c24b19affd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552200"
---
# <span data-ttu-id="0b8a7-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b8a7-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="0b8a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8a7-103">Ustawia stan celu konfiguracji reguł zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b8a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b8a7-104">SYNTAX</span></span>

### <span data-ttu-id="0b8a7-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0b8a7-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b8a7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b8a7-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b8a7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0b8a7-107">DESCRIPTION</span></span>
<span data-ttu-id="0b8a7-108">Polecenie cmdlet **Set-AzureRmNetworkSecurityRuleConfig** ustawia stan celu konfiguracji reguł zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="0b8a7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b8a7-109">EXAMPLES</span></span>

### <span data-ttu-id="0b8a7-110">Przykład 1. Zmienianie konfiguracji dostępu w regule zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="0b8a7-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="0b8a7-111">Pierwsze polecenie uzyskuje grupę zabezpieczeń sieci o nazwie NSG-fronton, a następnie zapisuje ją w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="0b8a7-112">Drugie polecenie używa operatora potoku w celu przekazania grupy zabezpieczeń w $nsg do polecenia Get-AzureRmNetworkSecurityRuleConfig, który uzyskuje konfigurację reguł zabezpieczeń o nazwie RDP-rule.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="0b8a7-113">W trzecim poleceniu jest zmieniana Konfiguracja dostępu protokołu RDP — reguła jest odrzucana.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="0b8a7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b8a7-114">PARAMETERS</span></span>

### <span data-ttu-id="0b8a7-115">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="0b8a7-115">-Access</span></span>
<span data-ttu-id="0b8a7-116">Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="0b8a7-117">Dopuszczalne wartości tego parametru to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="0b8a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8a7-118">-DefaultProfile</span></span>
<span data-ttu-id="0b8a7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b8a7-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="0b8a7-120">-Description</span></span>
<span data-ttu-id="0b8a7-121">Umożliwia określenie opisu konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="0b8a7-122">Maksymalny rozmiar to 140 znaków.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="0b8a7-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0b8a7-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="0b8a7-124">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="0b8a7-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b8a7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8a7-126">Adres międzydomenowy (Classless indomain Routing)</span><span class="sxs-lookup"><span data-stu-id="0b8a7-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="0b8a7-127">Zakres docelowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="0b8a7-127">A destination IP address range</span></span> 
- <span data-ttu-id="0b8a7-128">Znak wieloznaczny (\*), aby dopasować dowolny adres IP</span><span class="sxs-lookup"><span data-stu-id="0b8a7-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="0b8a7-129">Możesz korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="0b8a7-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b8a7-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="0b8a7-131">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0b8a7-132">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0b8a7-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0b8a7-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0b8a7-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="0b8a7-134">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0b8a7-135">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0b8a7-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0b8a7-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="0b8a7-136">-DestinationPortRange</span></span>
<span data-ttu-id="0b8a7-137">Określa port docelowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="0b8a7-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b8a7-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8a7-139">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="0b8a7-139">An integer</span></span> 
- <span data-ttu-id="0b8a7-140">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="0b8a7-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0b8a7-141">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="0b8a7-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0b8a7-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="0b8a7-142">-Direction</span></span>
<span data-ttu-id="0b8a7-143">Określa, czy reguła jest obliczana na potrzeby ruchu przychodzącego lub wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="0b8a7-144">Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="0b8a7-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b8a7-145">-Name</span></span>
<span data-ttu-id="0b8a7-146">Określa nazwę konfiguracji reguł zabezpieczeń sieci, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="0b8a7-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b8a7-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0b8a7-148">Określa obiekt **NetworkSecurityGroup** , który zawiera konfigurację reguł zabezpieczeń sieci do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8a7-149">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="0b8a7-149">-Priority</span></span>
<span data-ttu-id="0b8a7-150">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="0b8a7-151">Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="0b8a7-152">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="0b8a7-153">Niższy numer priorytetu, wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="0b8a7-154">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="0b8a7-154">-Protocol</span></span>
<span data-ttu-id="0b8a7-155">Określa protokół sieciowy, którego dotyczy konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="0b8a7-156">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b8a7-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="0b8a7-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="0b8a7-157">--Tcp</span></span>
- <span data-ttu-id="0b8a7-158">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="0b8a7-158">Udp</span></span>
- <span data-ttu-id="0b8a7-159">Znak wieloznaczny (\*) zgodny z obydwoma</span><span class="sxs-lookup"><span data-stu-id="0b8a7-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="0b8a7-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0b8a7-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="0b8a7-161">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="0b8a7-162">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b8a7-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8a7-163">CIDR</span><span class="sxs-lookup"><span data-stu-id="0b8a7-163">A CIDR</span></span>
- <span data-ttu-id="0b8a7-164">Zakres źródłowy adresu IP</span><span class="sxs-lookup"><span data-stu-id="0b8a7-164">A source IP range</span></span>
- <span data-ttu-id="0b8a7-165">Znak wieloznaczny (\*), aby dopasować dowolny adres IP</span><span class="sxs-lookup"><span data-stu-id="0b8a7-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="0b8a7-166">Możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="0b8a7-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b8a7-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="0b8a7-168">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="0b8a7-169">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0b8a7-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0b8a7-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0b8a7-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="0b8a7-171">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="0b8a7-172">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0b8a7-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0b8a7-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="0b8a7-173">-SourcePortRange</span></span>
<span data-ttu-id="0b8a7-174">Określa port źródłowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-174">Specifies the source port or range.</span></span>
<span data-ttu-id="0b8a7-175">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b8a7-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b8a7-176">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="0b8a7-176">An integer</span></span>
- <span data-ttu-id="0b8a7-177">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="0b8a7-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0b8a7-178">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="0b8a7-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0b8a7-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8a7-179">CommonParameters</span></span>
<span data-ttu-id="0b8a7-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b8a7-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8a7-181">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b8a7-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8a7-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b8a7-182">INPUTS</span></span>

### <span data-ttu-id="0b8a7-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b8a7-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="0b8a7-184">Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0b8a7-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="0b8a7-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b8a7-185">OUTPUTS</span></span>

### <span data-ttu-id="0b8a7-186">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b8a7-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0b8a7-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b8a7-187">NOTES</span></span>

## <span data-ttu-id="0b8a7-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b8a7-188">RELATED LINKS</span></span>

[<span data-ttu-id="0b8a7-189">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b8a7-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0b8a7-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b8a7-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0b8a7-191">Nowe — AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b8a7-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0b8a7-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b8a7-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


