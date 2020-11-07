---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889550"
---
# Get-AzsUserSubscription

## STRESZCZENIe
Pobierz listę abonamentów użytkowników jako administrator.

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
Pobierz listę abonamentów użytkowników jako administrator.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsUserSubscription
```

Pobierz listę abonamentów użytkowników jako administrator.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription

## INFORMACYJN

## LINKI POKREWNE

