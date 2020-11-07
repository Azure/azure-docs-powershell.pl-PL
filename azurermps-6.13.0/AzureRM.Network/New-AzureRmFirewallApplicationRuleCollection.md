---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
ms.openlocfilehash: e5fbad2b63213af972260948439984754e9eaa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719085"
---
# New-AzureRmFirewallApplicationRuleCollection

## STRESZCZENIe
Tworzy kolekcję reguł aplikacji zapory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmFirewallApplicationRuleCollection** tworzy kolekcję reguł aplikacji zapory.

## Przykłady

### 1: Tworzenie kolekcji z jedną regułą
```
$rule1 = New-AzureRmFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

W tym przykładzie tworzona jest kolekcja z jednej reguły. Wszystkie dane zgodne z warunkami określonymi w $rule 1 będą dozwolone.
Pierwsza reguła dotyczy całego ruchu HTTPS w porcie 443 od 10.0.0.0. Jeśli istnieje inna Kolekcja reguł aplikacji o wyższym priorytecie (mniejsza liczba), która również jest zgodna z ruchem zidentyfikowanym w $rule 1, w zamian będzie obowiązywać działanie kolekcji reguł o wyższym priorytecie. 

### 2: Dodawanie reguły do kolekcji reguł
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł aplikacji za pomocą jednej reguły, a następnie dodanie drugiej reguły do kolekcji reguł przy użyciu metody AddRule w obiekcie kolekcji reguł. Każda nazwa reguły w danej kolekcji reguł musi mieć unikatową nazwę i nie uwzględnia wielkości liter.

### 3: uzyskiwanie reguły z kolekcji reguł
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

W tym przykładzie jest tworzona nowa kolekcja reguł aplikacji z dowolną regułą, a następnie jest ona pobierana według nazwy, która jest wywoływana przez metodę GetRuleByName w obiekcie kolekcji reguł. W nazwie reguły dla metody GetRuleByName jest uwzględniana wielkość liter.

### 4: Usuwanie reguły z kolekcji reguł
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

W tym przykładzie przedstawiono tworzenie nowej kolekcji reguł aplikacji z dwiema regułami, a następnie usunięcie pierwszej reguły z kolekcji reguł przez połączenie metody RemoveRuleByName w obiekcie kolekcji reguł. W nazwie reguły dla metody RemoveRuleByName jest uwzględniana wielkość liter.

## PARAMETRÓW

### -ActionType
Akcja kolekcji reguł

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
Określa nazwę tej reguły aplikacji. Nazwa musi być unikatowa w kolekcji reguł.

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

### -Priority (priorytet)
Określa priorytet tej reguły. Priority to liczba z zakresu od 100 do 65000. Im mniejsza liczba, tym większy priorytet.

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

### — Reguła
Określa listę reguł, które mają być grupowane w tej kolekcji.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSFirewallApplicationRuleCollection

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmFirewallApplicationRule](./New-AzureRmFirewallApplicationRule.md)

[Nowe — AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)
