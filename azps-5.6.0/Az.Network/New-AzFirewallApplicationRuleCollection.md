---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: c82b150dd10a293bda1a001e4b930bcc2fe7989b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015034"
---
# New-AzFirewallApplicationRuleCollection

## SYNOPSIS
Tworzy kolekcję reguł aplikacji zapory.

## SKŁADNIA

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzFirewallApplicationRuleCollection** tworzy kolekcję reguł aplikacji zapory.

## PRZYKŁADY

### Przykład 1. Tworzenie kolekcji przy użyciu jednej reguły
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

W tym przykładzie jest tworzyna kolekcja z jedną regułą. Dozwolony będzie cały ruch ruchu, który jest $rule 1.
Pierwsza reguła dotyczy całego ruchu HTTPS na porcie 443 z 10.0.0.0. Jeśli istnieje inny zbiór reguł aplikacji o wyższym priorytecie (mniejsza liczba), który jest również taki, jak w przypadku ruchu wskazanego w programie $rule 1, zamiast tego zostanie wprowadzone działanie kolekcji reguł o wyższym priorytecie. 

### Przykład 2. Dodawanie reguły do kolekcji reguł
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

W tym przykładzie jest tworzyna nowa kolekcja reguł aplikacji z jedną regułą, a następnie do kolekcji reguł jest dodawania drugiej reguły przy użyciu metody AddRule dla obiektu kolekcji reguł. Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i jest bez uwzględniania liter.

### Przykład 3. Pobieranie reguły z kolekcji reguł
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

W tym przykładzie jest podmiotem tworzącym nową kolekcję reguł aplikacji z jedną regułą, która następnie pobiera regułę według nazwy (metody wywoływania GetRuleByName) dla obiektu kolekcji reguł. Nazwa reguły metody GetRuleByName jest bez uwzględniania liter.

### Przykład 4. Usuwanie reguły z kolekcji reguł
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

W tym przykładzie jest tworzena nowa kolekcja reguł aplikacji z dwiema regułami, a następnie pierwsza reguła jest usuwana z kolekcji reguł przez wywoływanie metody RemoveRuleByName w obiekcie kolekcji reguł. Nazwa reguły metody RemoveRuleByName jest bez uwzględniania liter.

## PARAMETERS

### - ActionType
Akcja zbioru reguł

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Nazwa
Określa nazwę tej reguły aplikacji. Nazwa musi być unikatowa w zbiorze reguł.

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

### — Priority (Priorytet)
Określa priorytet tej reguły. Priorytet to liczba od 100 do 65 000. Im mniejsza jest liczba, tym większy priorytet.

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

### — reguła
Określa listę reguł do zgrupowania w tej kolekcji.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection

## NOTATKI

## LINKI POKREWNE

[New-AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[New-AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
