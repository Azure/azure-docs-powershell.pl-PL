---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889553"
---
# Move-AzsSubscription

## STRESZCZENIe
Przenoszenie subskrypcji między delegowanymi ofertami dostawców.

## POLECENIA

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## Opis
Przenoszenie subskrypcji między delegowanymi ofertami dostawców.
Proces ten przeprowadza tylko ponowne znakowanie, ale nie spowoduje zmiany podstawowych ofert, planów, przydziałów dla abonamentów.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Move user subscriptions to a delegated provider offer.
```

Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-ResourceID "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/subscriptions/45ec4d39-8dea-4d26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

### --------------------------PRZYKŁAD 2--------------------------
```
Move user subscriptions from a delegated provider to the Default Provider.
```

$resourceIds = Get-AzsUserSubscription-Filter "offername EQ" O1 "" | gdzie {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | SELECT-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds

## PARAMETRÓW

### -AsJob
Określa, czy operacja przenoszenia ma być wykonywana jako zadanie.

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

### -DestinationDelegatedProviderOffer
Określa w pełni kwalifikowane delegowane dostawcy, do których to polecenie cmdlet przeniesie subskrypcje.
NULL, jeśli abonamenty mają być przenoszone z powrotem do domyślnego dostawcy.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Określa tablicę identyfikatorów zasobów abonamentu, które są przenoszone w pełni kwalifikowanego polecenia.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

