---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 2309d49dcd91ddefbcbe0e40379a759d50d5ba2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899104"
---
# New-AzureRmRouteFilterRuleConfig

## STRESZCZENIe
Tworzy regułę filtru tras dla filtru tras.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzureRmRouteFilterRuleConfig powoduje utworzenie reguły filtru tras dla filtru tras platformy Azure.

## Przykłady

### Przykład 1
```
PS C:\> {{ Add example code here }}
```

{{Dodaj opis przykładu}}

## PARAMETRÓW

### — Dostęp
Dostęp do reguły filtrowania tras.
Prawidłowe wartości to allow lub Deny.

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

### -CommunityList
Lista wartości społeczności, według której filtr trasy będzie filtrować.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

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

### -Force
Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę reguły filtru tras.

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

### -RouteFilterRuleType
Typ reguły filtrowania tras.
Prawidłowe wartości: społeczność

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSRouteFilterRule

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking

## LINKI POKREWNE

[Dodaj-AzureRmRouteFilterRuleConfig](./Add-AzureRmRouteFilterRuleConfig.md)

[Get-AzureRmRouteFilterRuleConfig](./Get-AzureRmRouteFilterRuleConfig.md)

[Remove-AzureRmRouteFilterRuleConfig](./Remove-AzureRmRouteFilterRuleConfig.md)

[Set-AzureRmRouteFilterRuleConfig](./Set-AzureRmRouteFilterRuleConfig.md)

