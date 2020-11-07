---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: edf783daa552cee1de48f0ea4992f28d79a23e24
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894154"
---
# <span data-ttu-id="bc214-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bc214-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="bc214-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc214-102">SYNOPSIS</span></span>
<span data-ttu-id="bc214-103">Tworzy kolekcję reguł aplikacji zapory.</span><span class="sxs-lookup"><span data-stu-id="bc214-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="bc214-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc214-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc214-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc214-105">DESCRIPTION</span></span>
<span data-ttu-id="bc214-106">Polecenie cmdlet **New-AzFirewallApplicationRuleCollection** tworzy kolekcję reguł aplikacji zapory.</span><span class="sxs-lookup"><span data-stu-id="bc214-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="bc214-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc214-107">EXAMPLES</span></span>

### <span data-ttu-id="bc214-108">1: Tworzenie kolekcji z jedną regułą</span><span class="sxs-lookup"><span data-stu-id="bc214-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="bc214-109">W tym przykładzie tworzona jest kolekcja z jednej reguły.</span><span class="sxs-lookup"><span data-stu-id="bc214-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="bc214-110">Wszystkie dane zgodne z warunkami określonymi w $rule 1 będą dozwolone.</span><span class="sxs-lookup"><span data-stu-id="bc214-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="bc214-111">Pierwsza reguła dotyczy całego ruchu HTTPS w porcie 443 od 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="bc214-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="bc214-112">Jeśli istnieje inna Kolekcja reguł aplikacji o wyższym priorytecie (mniejsza liczba), która również jest zgodna z ruchem zidentyfikowanym w $rule 1, w zamian będzie obowiązywać działanie kolekcji reguł o wyższym priorytecie.</span><span class="sxs-lookup"><span data-stu-id="bc214-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="bc214-113">2: Dodawanie reguły do kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="bc214-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="bc214-114">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł aplikacji za pomocą jednej reguły, a następnie dodanie drugiej reguły do kolekcji reguł przy użyciu metody AddRule w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="bc214-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="bc214-115">Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i nie uwzględnia wielkości liter.</span><span class="sxs-lookup"><span data-stu-id="bc214-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="bc214-116">3: uzyskiwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="bc214-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="bc214-117">W tym przykładzie jest tworzona nowa kolekcja reguł aplikacji z dowolną regułą, a następnie jest ona pobierana według nazwy, która jest wywoływana przez metodę GetRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="bc214-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="bc214-118">W nazwie reguły dla metody GetRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="bc214-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="bc214-119">4: Usuwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="bc214-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="bc214-120">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł aplikacji z dwiema regułami, a następnie usunięcie pierwszej reguły z kolekcji reguł przez połączenie metody RemoveRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="bc214-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="bc214-121">W nazwie reguły dla metody RemoveRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="bc214-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="bc214-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc214-122">PARAMETERS</span></span>

### <span data-ttu-id="bc214-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="bc214-123">-ActionType</span></span>
<span data-ttu-id="bc214-124">Akcja kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="bc214-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="bc214-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc214-125">-DefaultProfile</span></span>
<span data-ttu-id="bc214-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc214-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc214-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc214-127">-Name</span></span>
<span data-ttu-id="bc214-128">Określa nazwę tej reguły aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc214-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="bc214-129">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="bc214-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="bc214-130">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="bc214-130">-Priority</span></span>
<span data-ttu-id="bc214-131">Określa priorytet tej reguły.</span><span class="sxs-lookup"><span data-stu-id="bc214-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="bc214-132">Priority to liczba z zakresu od 100 do 65000.</span><span class="sxs-lookup"><span data-stu-id="bc214-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="bc214-133">Im mniejsza liczba, tym większy priorytet.</span><span class="sxs-lookup"><span data-stu-id="bc214-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="bc214-134">— Reguła</span><span class="sxs-lookup"><span data-stu-id="bc214-134">-Rule</span></span>
<span data-ttu-id="bc214-135">Określa listę reguł, które mają być grupowane w tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="bc214-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc214-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc214-136">-Confirm</span></span>
<span data-ttu-id="bc214-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc214-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc214-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc214-138">-WhatIf</span></span>
<span data-ttu-id="bc214-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc214-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc214-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bc214-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc214-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc214-141">CommonParameters</span></span>
<span data-ttu-id="bc214-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc214-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc214-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc214-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc214-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc214-144">INPUTS</span></span>

### <span data-ttu-id="bc214-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bc214-145">None</span></span>

## <span data-ttu-id="bc214-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc214-146">OUTPUTS</span></span>

### <span data-ttu-id="bc214-147">Microsoft. Azure. Commands. Network. models. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bc214-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="bc214-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc214-148">NOTES</span></span>

## <span data-ttu-id="bc214-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc214-149">RELATED LINKS</span></span>

[<span data-ttu-id="bc214-150">Nowe — AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="bc214-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="bc214-151">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc214-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="bc214-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc214-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
