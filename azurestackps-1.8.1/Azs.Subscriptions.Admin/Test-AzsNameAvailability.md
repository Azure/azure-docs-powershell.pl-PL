---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889985"
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Subscriptions. admin. models. CheckNameAvailabilityResponse

## INFORMACYJN

## LINKI POKREWNE

