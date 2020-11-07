---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719086"
---
# New-AzureRmFirewallApplicationRule

## STRESZCZENIe
Tworzy regułę aplikacji zapory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### TargetFqdn (domyślny)
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FqdnTag
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmFirewallApplicationRule** umożliwia utworzenie reguły aplikacji dla zapory systemu Azure.

## Przykłady

### 1: Tworzenie reguły zezwalającej na cały ruch HTTPS od 10.0.0.0
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

W tym przykładzie jest tworzona reguła zezwalająca na cały ruch HTTPS na porcie 443 od 10.0.0.0.

### 2: Tworzenie reguły zezwalającej na obsługę usługi WindowsUpdate dla podsieci 10.0.0.0/24
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

W tym przykładzie jest tworzona reguła zezwalająca na ruch w usłudze Windows updates dla domeny 10.0.0.0/24.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### — Opis
Umożliwia określenie opcjonalnego opisu tej reguły.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FqdnTag
Określa listę tagów FQDN dla tej reguły. Dostępne Tagi można pobrać przy użyciu polecenia cmdlet [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) .

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
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

### -Protocol (protokół)
Określa typ ruchu, który ma być filtrowany przez tę regułę. Format <protocol type> : <port> . Na przykład "http: 80" lub "https: 443".
Protokół jest obowiązkowy, gdy jest używana TargetFqdn, ale nie można go użyć z FqdnTag. Obsługiwane protokoły to HTTP i HTTPS.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
Adresy źródłowe reguły

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFqdn
Określa listę nazw domen filtrowanych według tej reguły.
Znak pomocą funkcji ' *' jest akceptowany tylko jako pierwszy znak nazwy FQDN na liście. W przypadku użycia pomocą funkcji uwzględnia dowolną liczbę znaków. (na przykład "* MSN.com" będzie pasować MSN.com i wszystkie jej poddomeny)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSFirewallApplicationRule

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmFirewallApplicationRuleCollection](./New-AzureRmFirewallApplicationRuleCollection.md)

[Nowe — AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md)
