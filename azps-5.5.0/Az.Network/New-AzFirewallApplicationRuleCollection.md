---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240826"
---
# <span data-ttu-id="b92fc-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b92fc-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="b92fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b92fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b92fc-103">Tworzy kolekcję reguł aplikacji zapory.</span><span class="sxs-lookup"><span data-stu-id="b92fc-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="b92fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b92fc-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b92fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b92fc-105">DESCRIPTION</span></span>
<span data-ttu-id="b92fc-106">Polecenie **cmdlet New-AzFirewallApplicationRuleCollection** tworzy kolekcję reguł aplikacji zapory.</span><span class="sxs-lookup"><span data-stu-id="b92fc-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="b92fc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b92fc-107">EXAMPLES</span></span>

### <span data-ttu-id="b92fc-108">Przykład 1. Tworzenie kolekcji przy użyciu jednej reguły</span><span class="sxs-lookup"><span data-stu-id="b92fc-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="b92fc-109">W tym przykładzie jest tworzyna kolekcja z jedną regułą.</span><span class="sxs-lookup"><span data-stu-id="b92fc-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="b92fc-110">Dozwolony będzie cały ruch, który jest zgodnie z warunkami $rule 1.</span><span class="sxs-lookup"><span data-stu-id="b92fc-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="b92fc-111">Pierwsza reguła dotyczy całego ruchu HTTPS na porcie 443 z 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b92fc-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="b92fc-112">Jeśli istnieje inny zbiór reguł aplikacji o wyższym priorytecie (mniejsza liczba), który również odpowiada ruchu zidentyfikowanego w programie $rule 1, zamiast tego zostanie wprowadzone działanie kolekcji reguł o wyższym priorytecie.</span><span class="sxs-lookup"><span data-stu-id="b92fc-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="b92fc-113">Przykład 2. Dodawanie reguły do zbioru reguł</span><span class="sxs-lookup"><span data-stu-id="b92fc-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="b92fc-114">W tym przykładzie jest tworzyna nowa kolekcja reguł aplikacji z jedną regułą, a następnie do kolekcji reguł jest dodawania drugiej reguły przy użyciu metody AddRule dla obiektu kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b92fc-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="b92fc-115">Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b92fc-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="b92fc-116">Przykład 3. Pobieranie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="b92fc-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="b92fc-117">W tym przykładzie jest podmiotem tworzącym nową kolekcję reguł aplikacji z jedną regułą, która następnie pobiera regułę według nazwy (metody wywoływania GetRuleByName) dla obiektu kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b92fc-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="b92fc-118">Nazwa reguły metody GetRuleByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b92fc-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="b92fc-119">Przykład 4. Usuwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="b92fc-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="b92fc-120">W tym przykładzie jest tworzena nowa kolekcja reguł aplikacji z dwiema regułami, a następnie pierwsza reguła jest usuwana z kolekcji reguł przez wywoływanie metody RemoveRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b92fc-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="b92fc-121">Nazwa reguły metody RemoveRuleByName jest bez uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b92fc-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="b92fc-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b92fc-122">PARAMETERS</span></span>

### <span data-ttu-id="b92fc-123">- ActionType</span><span class="sxs-lookup"><span data-stu-id="b92fc-123">-ActionType</span></span>
<span data-ttu-id="b92fc-124">Akcja zbioru reguł</span><span class="sxs-lookup"><span data-stu-id="b92fc-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="b92fc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92fc-125">-DefaultProfile</span></span>
<span data-ttu-id="b92fc-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b92fc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b92fc-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b92fc-127">-Name</span></span>
<span data-ttu-id="b92fc-128">Określa nazwę tej reguły aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b92fc-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="b92fc-129">Nazwa musi być unikatowa w zbiorze reguł.</span><span class="sxs-lookup"><span data-stu-id="b92fc-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="b92fc-130">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="b92fc-130">-Priority</span></span>
<span data-ttu-id="b92fc-131">Określa priorytet tej reguły.</span><span class="sxs-lookup"><span data-stu-id="b92fc-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="b92fc-132">Priorytet to liczba od 100 do 65 000.</span><span class="sxs-lookup"><span data-stu-id="b92fc-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="b92fc-133">Im mniejsza jest liczba, tym większy priorytet.</span><span class="sxs-lookup"><span data-stu-id="b92fc-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="b92fc-134">— reguła</span><span class="sxs-lookup"><span data-stu-id="b92fc-134">-Rule</span></span>
<span data-ttu-id="b92fc-135">Określa listę reguł do zgrupowania w tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b92fc-135">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="b92fc-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b92fc-136">-Confirm</span></span>
<span data-ttu-id="b92fc-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b92fc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b92fc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b92fc-138">-WhatIf</span></span>
<span data-ttu-id="b92fc-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b92fc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b92fc-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b92fc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b92fc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92fc-141">CommonParameters</span></span>
<span data-ttu-id="b92fc-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b92fc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92fc-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b92fc-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92fc-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b92fc-144">INPUTS</span></span>

### <span data-ttu-id="b92fc-145">Brak</span><span class="sxs-lookup"><span data-stu-id="b92fc-145">None</span></span>

## <span data-ttu-id="b92fc-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b92fc-146">OUTPUTS</span></span>

### <span data-ttu-id="b92fc-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b92fc-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="b92fc-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b92fc-148">NOTES</span></span>

## <span data-ttu-id="b92fc-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b92fc-149">RELATED LINKS</span></span>

[<span data-ttu-id="b92fc-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b92fc-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="b92fc-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b92fc-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b92fc-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b92fc-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
