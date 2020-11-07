---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710763"
---
# Get-AzsUserSubscription

## STRESZCZENIe
Pobieranie listy abonamentów użytkowników jako operatora.

## POLECENIA

### Lista (domyślna)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## Opis
Pobieranie listy abonamentów użytkowników jako operatora.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsUserSubscription
```

Pobieranie listy abonamentów użytkowników jako operatora.

## PARAMETRÓW

### -Filter
Parametr filtru OData.

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subskrypcji
Parametr identyfikatora subskrypcji.

```yaml
Type: Guid
Parameter Sets: Get
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

### Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription

## INFORMACYJN

## LINKI POKREWNE

