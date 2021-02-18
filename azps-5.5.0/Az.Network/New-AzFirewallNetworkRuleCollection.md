---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240802"
---
# <span data-ttu-id="b6312-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6312-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="b6312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6312-102">SYNOPSIS</span></span>
<span data-ttu-id="b6312-103">Tworzy zbiór reguł sieciowych zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6312-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="b6312-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6312-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6312-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6312-105">DESCRIPTION</span></span>
<span data-ttu-id="b6312-106">Polecenie **cmdlet New-AzFirewallNetworkRuleCollection** tworzy kolekcję reguł sieciowych zapory.</span><span class="sxs-lookup"><span data-stu-id="b6312-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="b6312-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6312-107">EXAMPLES</span></span>

### <span data-ttu-id="b6312-108">Przykład 1. Tworzenie zbioru sieci z dwiema regułami</span><span class="sxs-lookup"><span data-stu-id="b6312-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="b6312-109">W tym przykładzie jest organizacji, która zezwala na cały ruch, który jest zgodnie z jedną z dwóch reguł.</span><span class="sxs-lookup"><span data-stu-id="b6312-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="b6312-110">Pierwsza reguła dotyczy całego ruchu UDP.</span><span class="sxs-lookup"><span data-stu-id="b6312-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="b6312-111">Druga reguła dotyczy ruchu TCP z 10.0.0.0 do 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="b6312-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="b6312-112">Jeśli istnieje inna kolekcja reguł sieciowych o wyższym priorytecie (mniejsza liczba), która również odpowiada ruchu zidentyfikowanego w programie $rule 1 lub $rule 2, zamiast tego będzie obowiązywać akcja zbioru reguł o wyższym priorytecie.</span><span class="sxs-lookup"><span data-stu-id="b6312-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="b6312-113">Przykład 2. Dodawanie reguły do zbioru reguł</span><span class="sxs-lookup"><span data-stu-id="b6312-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="b6312-114">W tym przykładzie jest tworzenie nowej kolekcji reguł sieciowych z jedną regułą, a następnie dodawania drugiej reguły do zbioru reguł przy użyciu metody AddRule dla obiektu kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b6312-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="b6312-115">Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b6312-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="b6312-116">Przykład 3. Pobieranie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="b6312-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="b6312-117">W tym przykładzie jest podmiotem tworzącym nową kolekcję reguł sieciowych z jedną regułą, która następnie pobiera regułę według nazwy (metody wywoływania GetRuleByName) dla obiektu kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b6312-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="b6312-118">Nazwa reguły metody GetRuleByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b6312-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="b6312-119">Przykład 4. Usuwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="b6312-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="b6312-120">W tym przykładzie jest tworzena nowa kolekcja reguł sieciowych z dwiema regułami, a następnie pierwsza reguła jest usuwana z kolekcji reguł przez wywoływanie metody RemoveRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b6312-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="b6312-121">Nazwa reguły metody RemoveRuleByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b6312-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="b6312-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6312-122">PARAMETERS</span></span>

### <span data-ttu-id="b6312-123">- ActionType</span><span class="sxs-lookup"><span data-stu-id="b6312-123">-ActionType</span></span>
<span data-ttu-id="b6312-124">Określa akcję, która ma zostać podjęta w celu dopasowania ruchu do warunków tej reguły.</span><span class="sxs-lookup"><span data-stu-id="b6312-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="b6312-125">Zaakceptowane akcje to "Zezwalaj" lub "Odmów".</span><span class="sxs-lookup"><span data-stu-id="b6312-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="b6312-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6312-126">-DefaultProfile</span></span>
<span data-ttu-id="b6312-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6312-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6312-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6312-128">-Name</span></span>
<span data-ttu-id="b6312-129">Określa nazwę tego zbioru reguł sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b6312-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="b6312-130">Nazwa musi być unikatowa we wszystkich regułach sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b6312-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="b6312-131">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="b6312-131">-Priority</span></span>
<span data-ttu-id="b6312-132">Określa priorytet tej kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b6312-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="b6312-133">Priorytet to liczba od 100 do 65 000.</span><span class="sxs-lookup"><span data-stu-id="b6312-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="b6312-134">Im mniejsza jest liczba, tym wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="b6312-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="b6312-135">— Reguła</span><span class="sxs-lookup"><span data-stu-id="b6312-135">-Rule</span></span>
<span data-ttu-id="b6312-136">Określa listę reguł do zgrupowania w tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b6312-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="b6312-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6312-137">-Confirm</span></span>
<span data-ttu-id="b6312-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b6312-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6312-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6312-139">-WhatIf</span></span>
<span data-ttu-id="b6312-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6312-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6312-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b6312-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6312-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6312-142">CommonParameters</span></span>
<span data-ttu-id="b6312-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6312-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6312-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6312-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6312-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6312-145">INPUTS</span></span>

### <span data-ttu-id="b6312-146">Brak</span><span class="sxs-lookup"><span data-stu-id="b6312-146">None</span></span>

## <span data-ttu-id="b6312-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6312-147">OUTPUTS</span></span>

### <span data-ttu-id="b6312-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6312-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="b6312-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6312-149">NOTES</span></span>

## <span data-ttu-id="b6312-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6312-150">RELATED LINKS</span></span>

[<span data-ttu-id="b6312-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b6312-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="b6312-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6312-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b6312-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6312-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
