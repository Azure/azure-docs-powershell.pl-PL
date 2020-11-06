---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523526"
---
# Get-AzsOffer

## STRESZCZENIe
Zapoznaj się z listą ofert publicznych.

## POLECENIA

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## Opis
Zapoznaj się z listą ofert publicznych.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsOffer | fl
```

Zapoznaj się z listą ofert publicznych.

## PARAMETRÓW

### -Skip
Pomijanie pierwszych N elementów określonych przez wartość parametru.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Początek
Zwraca N pierwszych elementów określonych przez wartość parametru.
Obowiązuje po parametrze-Skip.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Subscription. MODELES. Offer

## INFORMACYJN

## LINKI POKREWNE

