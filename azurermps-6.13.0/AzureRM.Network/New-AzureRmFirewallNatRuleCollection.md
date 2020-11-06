---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
ms.openlocfilehash: 12b45dd5fd62dabb2650f121f52a539962315513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541692"
---
# <span data-ttu-id="573dc-101">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="573dc-101">New-AzureRmFirewallNatRuleCollection</span></span>

## <span data-ttu-id="573dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="573dc-102">SYNOPSIS</span></span>
<span data-ttu-id="573dc-103">Tworzy kolekcję reguł NAT dla zapory.</span><span class="sxs-lookup"><span data-stu-id="573dc-103">Creates a collection of Firewall NAT rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="573dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="573dc-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="573dc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="573dc-105">DESCRIPTION</span></span>
<span data-ttu-id="573dc-106">Polecenie cmdlet **New-AzureRmFirewallNatRuleCollection** tworzy kolekcję reguł NAT dla zapory.</span><span class="sxs-lookup"><span data-stu-id="573dc-106">The **New-AzureRmFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="573dc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="573dc-107">EXAMPLES</span></span>

### <span data-ttu-id="573dc-108">1: Tworzenie kolekcji z jedną regułą</span><span class="sxs-lookup"><span data-stu-id="573dc-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="573dc-109">W tym przykładzie tworzona jest kolekcja z jednej reguły.</span><span class="sxs-lookup"><span data-stu-id="573dc-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="573dc-110">Cały ruch zgodny z warunkami określonymi w $rule 1 będzie DNAT'ed do przetłumaczonego adresu i portu.</span><span class="sxs-lookup"><span data-stu-id="573dc-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="573dc-111">2: Dodawanie reguły do kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="573dc-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="573dc-112">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł NAT za pomocą jednej reguły, a następnie dodanie drugiej reguły do kolekcji reguł przy użyciu metody AddRule w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="573dc-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="573dc-113">Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i nie uwzględnia wielkości liter.</span><span class="sxs-lookup"><span data-stu-id="573dc-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="573dc-114">3: uzyskiwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="573dc-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="573dc-115">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł NAT za pomocą jednej reguły, a następnie pobranie reguły przy użyciu nazwy, która GetRuleByName metodę na obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="573dc-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="573dc-116">W nazwie reguły dla metody GetRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="573dc-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="573dc-117">4: Usuwanie reguły z kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="573dc-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="573dc-118">W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł NAT z dwiema regułami, a następnie usunięcie pierwszej reguły z kolekcji reguł przez połączenie metody RemoveRuleByName w obiekcie kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="573dc-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="573dc-119">W nazwie reguły dla metody RemoveRuleByName jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="573dc-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="573dc-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="573dc-120">PARAMETERS</span></span>

### <span data-ttu-id="573dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573dc-121">-DefaultProfile</span></span>
<span data-ttu-id="573dc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="573dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573dc-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="573dc-123">-Name</span></span>
<span data-ttu-id="573dc-124">Określa nazwę tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="573dc-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="573dc-125">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="573dc-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="573dc-126">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="573dc-126">-Priority</span></span>
<span data-ttu-id="573dc-127">Określa priorytet tej reguły.</span><span class="sxs-lookup"><span data-stu-id="573dc-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="573dc-128">Priority to liczba z zakresu od 100 do 65000.</span><span class="sxs-lookup"><span data-stu-id="573dc-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="573dc-129">Im mniejsza liczba, tym większy priorytet.</span><span class="sxs-lookup"><span data-stu-id="573dc-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="573dc-130">— Reguła</span><span class="sxs-lookup"><span data-stu-id="573dc-130">-Rule</span></span>
<span data-ttu-id="573dc-131">Określa listę reguł, które mają być grupowane w tej kolekcji.</span><span class="sxs-lookup"><span data-stu-id="573dc-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573dc-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="573dc-132">-Confirm</span></span>
<span data-ttu-id="573dc-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="573dc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="573dc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573dc-134">-WhatIf</span></span>
<span data-ttu-id="573dc-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="573dc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573dc-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="573dc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="573dc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573dc-137">CommonParameters</span></span>
<span data-ttu-id="573dc-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573dc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573dc-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573dc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573dc-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="573dc-140">INPUTS</span></span>

### <span data-ttu-id="573dc-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="573dc-141">None</span></span>
<span data-ttu-id="573dc-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="573dc-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="573dc-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="573dc-143">OUTPUTS</span></span>

### <span data-ttu-id="573dc-144">Microsoft. Azure. Commands. Network. models. PSFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="573dc-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRuleCollection</span></span>

## <span data-ttu-id="573dc-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="573dc-145">NOTES</span></span>

## <span data-ttu-id="573dc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="573dc-146">RELATED LINKS</span></span>

[<span data-ttu-id="573dc-147">Nowe — AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="573dc-147">New-AzureRmFirewallNatRule</span></span>](./New-AzureRmFirewallNatRule.md)

[<span data-ttu-id="573dc-148">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="573dc-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="573dc-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="573dc-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
