---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: af0a81cf915cd853bfc8ca957d706cdb45d96180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709300"
---
# <span data-ttu-id="702fb-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="702fb-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="702fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="702fb-102">SYNOPSIS</span></span>
<span data-ttu-id="702fb-103">Tworzy zestaw reguł sieciowych dla usługi Zapora na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="702fb-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="702fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="702fb-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="702fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="702fb-105">DESCRIPTION</span></span>
<span data-ttu-id="702fb-106">Polecenie cmdlet **New-AzFirewallNetworkRuleCollection** tworzy kolekcję reguł sieci zapory.</span><span class="sxs-lookup"><span data-stu-id="702fb-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="702fb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="702fb-107">EXAMPLES</span></span>

### <span data-ttu-id="702fb-108">1: Tworzenie kolekcji sieciowej z dwiema regułami</span><span class="sxs-lookup"><span data-stu-id="702fb-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="702fb-109">W tym przykładzie przedstawiono tworzenie kolekcji, która umożliwia cały ruch zgodny z jedną z dwóch reguł.</span><span class="sxs-lookup"><span data-stu-id="702fb-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="702fb-110">Pierwsza reguła dotyczy całego ruchu w ramach protokołu UDP.</span><span class="sxs-lookup"><span data-stu-id="702fb-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="702fb-111">Druga reguła dotyczy ruchu TCP od 10.0.0.0 do 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="702fb-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="702fb-112">Jeśli istnieje inna Kolekcja reguł sieci o wyższym priorytecie (mniejsza liczba), która również jest zgodna z ruchem określonym w $rule 1 lub $rule 2, zamiast tego zostanie wykorzystana akcja kolekcji reguł o wyższym priorytecie.</span><span class="sxs-lookup"><span data-stu-id="702fb-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="702fb-113">2: Dodawanie reguły do kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="702fb-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="702fb-114">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł sieci z zadaną regułą, a następnie dodanie drugiej reguły do kolekcji reguł przy użyciu metody AddRule w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="702fb-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="702fb-115">Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i nie uwzględnia wielkości liter.</span><span class="sxs-lookup"><span data-stu-id="702fb-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="702fb-116">3: uzyskiwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="702fb-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="702fb-117">W tym przykładzie jest tworzona nowa kolekcja reguł sieci z zadaną regułą, a następnie jest ona pobierana według nazwy, która jest wywoływana przez metodę GetRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="702fb-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="702fb-118">W nazwie reguły dla metody GetRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="702fb-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="702fb-119">4: Usuwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="702fb-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="702fb-120">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł sieci z dwiema regułami, a następnie usunięcie pierwszej reguły z kolekcji reguł przez połączenie metody RemoveRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="702fb-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="702fb-121">W nazwie reguły dla metody RemoveRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="702fb-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="702fb-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="702fb-122">PARAMETERS</span></span>

### <span data-ttu-id="702fb-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="702fb-123">-ActionType</span></span>
<span data-ttu-id="702fb-124">Określa akcję, którą należy podjąć w przypadku warunków zgodnych z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="702fb-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="702fb-125">Akceptowane akcje to "Zezwalaj" lub "Odmów".</span><span class="sxs-lookup"><span data-stu-id="702fb-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="702fb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="702fb-126">-DefaultProfile</span></span>
<span data-ttu-id="702fb-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="702fb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="702fb-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="702fb-128">-Name</span></span>
<span data-ttu-id="702fb-129">Określa nazwę tej kolekcji reguł sieci.</span><span class="sxs-lookup"><span data-stu-id="702fb-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="702fb-130">Nazwa musi być unikatowa we wszystkich kolekcjach reguł sieci.</span><span class="sxs-lookup"><span data-stu-id="702fb-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="702fb-131">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="702fb-131">-Priority</span></span>
<span data-ttu-id="702fb-132">Określa priorytet tej kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="702fb-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="702fb-133">Priority to liczba z zakresu od 100 do 65000.</span><span class="sxs-lookup"><span data-stu-id="702fb-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="702fb-134">Im mniejsza liczba, tym wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="702fb-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="702fb-135">— Reguła</span><span class="sxs-lookup"><span data-stu-id="702fb-135">-Rule</span></span>
<span data-ttu-id="702fb-136">Określa listę reguł, które mają być grupowane w tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="702fb-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="702fb-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="702fb-137">-Confirm</span></span>
<span data-ttu-id="702fb-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="702fb-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="702fb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="702fb-139">-WhatIf</span></span>
<span data-ttu-id="702fb-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="702fb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="702fb-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="702fb-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="702fb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702fb-142">CommonParameters</span></span>
<span data-ttu-id="702fb-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="702fb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702fb-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="702fb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702fb-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="702fb-145">INPUTS</span></span>

### <span data-ttu-id="702fb-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="702fb-146">None</span></span>

## <span data-ttu-id="702fb-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="702fb-147">OUTPUTS</span></span>

### <span data-ttu-id="702fb-148">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="702fb-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="702fb-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="702fb-149">NOTES</span></span>

## <span data-ttu-id="702fb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="702fb-150">RELATED LINKS</span></span>

[<span data-ttu-id="702fb-151">Nowe — AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="702fb-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="702fb-152">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="702fb-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="702fb-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="702fb-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)