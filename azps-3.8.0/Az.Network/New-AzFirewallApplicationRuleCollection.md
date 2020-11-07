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
# New-AzFirewallApplicationRuleCollection

## STRESZCZENIe
Tworzy kolekcję reguł aplikacji zapory.

## POLECENIA

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzFirewallApplicationRuleCollection** tworzy kolekcję reguł aplikacji zapory.

## Przykłady

### 1: Tworzenie kolekcji z jedną regułą
```
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

W tym przykładzie tworzona jest kolekcja z jednej reguły. Wszystkie dane zgodne z warunkami określonymi w $rule 1 będą dozwolone.
Pierwsza reguła dotyczy całego ruchu HTTPS w porcie 443 od 10.0.0.0. Jeśli istnieje inna Kolekcja reguł aplikacji o wyższym priorytecie (mniejsza liczba), która również jest zgodna z ruchem zidentyfikowanym w $rule 1, w zamian będzie obowiązywać działanie kolekcji reguł o wyższym priorytecie. 

### 2: Dodawanie reguły do kolekcji reguł
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł aplikacji za pomocą jednej reguły, a następnie dodanie drugiej reguły do kolekcji reguł przy użyciu metody AddRule w obiekcie kolekcji reguł. Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i nie uwzględnia wielkości liter.

### 3: uzyskiwanie reguły z kolekcji reguł
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

W tym przykładzie jest tworzona nowa kolekcja reguł aplikacji z dowolną regułą, a następnie jest ona pobierana według nazwy, która jest wywoływana przez metodę GetRuleByName w obiekcie kolekcji reguł. W nazwie reguły dla metody GetRuleByName jest uwzględniana wielkość liter.

### 4: Usuwanie reguły z kolekcji reguł
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł aplikacji z dwiema regułami, a następnie usunięcie pierwszej reguły z kolekcji reguł przez połączenie metody RemoveRuleByName w obiekcie kolekcji reguł. W nazwie reguły dla metody RemoveRuleByName jest uwzględniana wielkość liter.

## PARAMETRÓW

### -ActionType
Akcja kolekcji reguł

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
Określa nazwę tej reguły aplikacji. Nazwa musi być unikatowa w kolekcji reguł.

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

### -Priority (priorytet)
Określa priorytet tej reguły. Priority to liczba z zakresu od 100 do 65000. Im mniejsza liczba, tym większy priorytet.

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

### — Reguła
Określa listę reguł, które mają być grupowane w tej kolekcji.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSAzureFirewallApplicationRuleCollection

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[Nowe — AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
