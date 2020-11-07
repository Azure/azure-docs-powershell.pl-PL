---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888086"
---
# Test-AzsNameAvailability

## STRESZCZENIe
Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.

## POLECENIA

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## Opis
Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

Zwraca wartość Avaialbility określonego typu i nazwy zasobu subskrypcji.

## PARAMETRÓW

### -Name (nazwa)
Nazwa zasobu do zweryfikowania.

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

### -ResourceType
Typ zasobu do zweryfikowania.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Subscriptions. admin. models. CheckNameAvailabilityResponse

## INFORMACYJN

## LINKI POKREWNE

