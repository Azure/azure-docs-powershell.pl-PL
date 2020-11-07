---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889250"
---
# Get-AzsSubscriptionsQuota

## STRESZCZENIe
Pobieranie listy przydziałów dostawców zasobów abonamentu w lokalizacji.

## POLECENIA

### Lista (domyślna)
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## Opis
Pobieranie listy przydziałów w lokalizacji.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsSubscriptionsQuota
```

Pobieranie listy przydziałów dostawców zasobów abonamentu w lokalizacji.

## PARAMETRÓW

### — Lokalizacja
Lokalizacja AzureStack.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa przydziału.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Subscriptions. admin. modele. przydział

## INFORMACYJN

## LINKI POKREWNE

