---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523609"
---
# Close-AzsAlert

## STRESZCZENIe
Zamyka dany alert.

## POLECENIA

### Zamknij (domyślne)
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Inputobject
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Zasobów
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Zamyka dany alert.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

Zamknij alert według nazwy.

### --------------------------PRZYKŁAD 2--------------------------
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

Zamykanie alertu za pośrednictwem połączenia rurowego.

## PARAMETRÓW

### -Force
Nie pytaj o potwierdzenie.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Alert zwrócony w wyniku Get-AzsAlert.

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Lokalizacja
Nazwa lokalizacji.

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Identyfikator alertu.

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, w której znajduje się dany zasób.

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. alert

## INFORMACYJN

## LINKI POKREWNE

