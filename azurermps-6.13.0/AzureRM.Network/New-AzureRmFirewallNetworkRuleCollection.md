---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
ms.openlocfilehash: 79ead5ac618b4631c3ec790156fe1a75e4169882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547460"
---
# <span data-ttu-id="529dd-101">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="529dd-101">New-AzureRmFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="529dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="529dd-102">SYNOPSIS</span></span>
<span data-ttu-id="529dd-103">Tworzy zestaw reguł sieciowych dla usługi Zapora na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="529dd-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="529dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="529dd-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="529dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="529dd-105">DESCRIPTION</span></span>
<span data-ttu-id="529dd-106">Polecenie cmdlet **New-AzureRmFirewallNetworkRuleCollection** tworzy kolekcję reguł sieci zapory.</span><span class="sxs-lookup"><span data-stu-id="529dd-106">The **New-AzureRmFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="529dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="529dd-107">EXAMPLES</span></span>

### <span data-ttu-id="529dd-108">1: Tworzenie kolekcji sieciowej z dwiema regułami</span><span class="sxs-lookup"><span data-stu-id="529dd-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzureRmFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="529dd-109">W tym przykładzie przedstawiono tworzenie kolekcji, która umożliwia cały ruch zgodny z jedną z dwóch reguł.</span><span class="sxs-lookup"><span data-stu-id="529dd-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="529dd-110">Pierwsza reguła dotyczy całego ruchu w ramach protokołu UDP.</span><span class="sxs-lookup"><span data-stu-id="529dd-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="529dd-111">Druga reguła dotyczy ruchu TCP od 10.0.0.0 do 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="529dd-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="529dd-112">Jeśli istnieje inna Kolekcja reguł sieci o wyższym priorytecie (mniejsza liczba), która również jest zgodna z ruchem określonym w $rule 1 lub $rule 2, zamiast tego zostanie wykorzystana akcja kolekcji reguł o wyższym priorytecie.</span><span class="sxs-lookup"><span data-stu-id="529dd-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="529dd-113">2: Dodawanie reguły do kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="529dd-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="529dd-114">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł sieci z zadaną regułą, a następnie dodanie drugiej reguły do kolekcji reguł przy użyciu metody AddRule w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="529dd-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="529dd-115">Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i nie uwzględnia wielkości liter.</span><span class="sxs-lookup"><span data-stu-id="529dd-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="529dd-116">3: uzyskiwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="529dd-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="529dd-117">W tym przykładzie jest tworzona nowa kolekcja reguł sieci z zadaną regułą, a następnie jest ona pobierana według nazwy, która jest wywoływana przez metodę GetRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="529dd-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="529dd-118">W nazwie reguły dla metody GetRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="529dd-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="529dd-119">4: Usuwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="529dd-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="529dd-120">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł sieci z dwiema regułami, a następnie usunięcie pierwszej reguły z kolekcji reguł przez połączenie metody RemoveRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="529dd-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="529dd-121">W nazwie reguły dla metody RemoveRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="529dd-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="529dd-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="529dd-122">PARAMETERS</span></span>

### <span data-ttu-id="529dd-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="529dd-123">-ActionType</span></span>
<span data-ttu-id="529dd-124">Określa akcję, którą należy podjąć w przypadku warunków zgodnych z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="529dd-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="529dd-125">Akceptowane akcje to "Zezwalaj" lub "Odmów".</span><span class="sxs-lookup"><span data-stu-id="529dd-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529dd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529dd-126">-DefaultProfile</span></span>
<span data-ttu-id="529dd-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="529dd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="529dd-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="529dd-128">-Name</span></span>
<span data-ttu-id="529dd-129">Określa nazwę tej kolekcji reguł sieci.</span><span class="sxs-lookup"><span data-stu-id="529dd-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="529dd-130">Nazwa musi być unikatowa we wszystkich kolekcjach reguł sieci.</span><span class="sxs-lookup"><span data-stu-id="529dd-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="529dd-131">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="529dd-131">-Priority</span></span>
<span data-ttu-id="529dd-132">Określa priorytet tej kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="529dd-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="529dd-133">Priority to liczba z zakresu od 100 do 65000.</span><span class="sxs-lookup"><span data-stu-id="529dd-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="529dd-134">Im mniejsza liczba, tym wyższy priorytet.</span><span class="sxs-lookup"><span data-stu-id="529dd-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529dd-135">— Reguła</span><span class="sxs-lookup"><span data-stu-id="529dd-135">-Rule</span></span>
<span data-ttu-id="529dd-136">Określa listę reguł, które mają być grupowane w tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="529dd-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529dd-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="529dd-137">-Confirm</span></span>
<span data-ttu-id="529dd-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="529dd-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529dd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="529dd-139">-WhatIf</span></span>
<span data-ttu-id="529dd-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="529dd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="529dd-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="529dd-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529dd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529dd-142">CommonParameters</span></span>
<span data-ttu-id="529dd-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529dd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529dd-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529dd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529dd-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="529dd-145">INPUTS</span></span>

### <span data-ttu-id="529dd-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="529dd-146">None</span></span>
<span data-ttu-id="529dd-147">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="529dd-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="529dd-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="529dd-148">OUTPUTS</span></span>

### <span data-ttu-id="529dd-149">Microsoft. Azure. Commands. Network. models. PSFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="529dd-149">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="529dd-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="529dd-150">NOTES</span></span>

## <span data-ttu-id="529dd-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="529dd-151">RELATED LINKS</span></span>

[<span data-ttu-id="529dd-152">Nowe — AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="529dd-152">New-AzureRmFirewallNetworkRule</span></span>](./New-AzureRmFirewallNetworkRule.md)

[<span data-ttu-id="529dd-153">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="529dd-153">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="529dd-154">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="529dd-154">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
