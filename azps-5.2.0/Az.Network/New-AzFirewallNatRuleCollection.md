---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347677"
---
# <span data-ttu-id="8266c-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8266c-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="8266c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8266c-102">SYNOPSIS</span></span>
<span data-ttu-id="8266c-103">Tworzy kolekcję reguł NAT dla zapory.</span><span class="sxs-lookup"><span data-stu-id="8266c-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="8266c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8266c-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8266c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8266c-105">DESCRIPTION</span></span>
<span data-ttu-id="8266c-106">Polecenie cmdlet **New-AzFirewallNatRuleCollection** tworzy kolekcję reguł NAT dla zapory.</span><span class="sxs-lookup"><span data-stu-id="8266c-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="8266c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8266c-107">EXAMPLES</span></span>

### <span data-ttu-id="8266c-108">Przykład 1. Tworzenie kolekcji z jedną regułą</span><span class="sxs-lookup"><span data-stu-id="8266c-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="8266c-109">W tym przykładzie tworzona jest kolekcja z jednej reguły.</span><span class="sxs-lookup"><span data-stu-id="8266c-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="8266c-110">Cały ruch zgodny z warunkami określonymi w $rule 1 będzie DNAT'ed do przetłumaczonego adresu i portu.</span><span class="sxs-lookup"><span data-stu-id="8266c-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="8266c-111">Przykład 2: Dodawanie reguły do kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="8266c-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="8266c-112">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł NAT za pomocą jednej reguły, a następnie dodanie drugiej reguły do kolekcji reguł przy użyciu metody AddRule w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="8266c-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="8266c-113">Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i nie uwzględnia wielkości liter.</span><span class="sxs-lookup"><span data-stu-id="8266c-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="8266c-114">Przykład 3: uzyskiwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="8266c-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="8266c-115">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł NAT za pomocą jednej reguły, a następnie pobranie reguły przy użyciu nazwy, która GetRuleByName metodę na obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="8266c-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="8266c-116">W nazwie reguły dla metody GetRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8266c-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="8266c-117">Przykład 4: Usuwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="8266c-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="8266c-118">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł NAT z dwiema regułami, a następnie usunięcie pierwszej reguły z kolekcji reguł przez połączenie metody RemoveRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="8266c-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="8266c-119">W nazwie reguły dla metody RemoveRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8266c-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="8266c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8266c-120">PARAMETERS</span></span>

### <span data-ttu-id="8266c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8266c-121">-DefaultProfile</span></span>
<span data-ttu-id="8266c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8266c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8266c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8266c-123">-Name</span></span>
<span data-ttu-id="8266c-124">Określa nazwę tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="8266c-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="8266c-125">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="8266c-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="8266c-126">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="8266c-126">-Priority</span></span>
<span data-ttu-id="8266c-127">Określa priorytet tej reguły.</span><span class="sxs-lookup"><span data-stu-id="8266c-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="8266c-128">Priority to liczba z zakresu od 100 do 65000.</span><span class="sxs-lookup"><span data-stu-id="8266c-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="8266c-129">Im mniejsza liczba, tym większy priorytet.</span><span class="sxs-lookup"><span data-stu-id="8266c-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="8266c-130">— Reguła</span><span class="sxs-lookup"><span data-stu-id="8266c-130">-Rule</span></span>
<span data-ttu-id="8266c-131">Określa listę reguł, które mają być grupowane w tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="8266c-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8266c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8266c-132">-Confirm</span></span>
<span data-ttu-id="8266c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8266c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8266c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8266c-134">-WhatIf</span></span>
<span data-ttu-id="8266c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8266c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8266c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8266c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8266c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8266c-137">CommonParameters</span></span>
<span data-ttu-id="8266c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8266c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8266c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8266c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8266c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8266c-140">INPUTS</span></span>

### <span data-ttu-id="8266c-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8266c-141">None</span></span>

## <span data-ttu-id="8266c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8266c-142">OUTPUTS</span></span>

### <span data-ttu-id="8266c-143">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8266c-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="8266c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8266c-144">NOTES</span></span>

## <span data-ttu-id="8266c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8266c-145">RELATED LINKS</span></span>

[<span data-ttu-id="8266c-146">Nowe — AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="8266c-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="8266c-147">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8266c-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="8266c-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8266c-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
