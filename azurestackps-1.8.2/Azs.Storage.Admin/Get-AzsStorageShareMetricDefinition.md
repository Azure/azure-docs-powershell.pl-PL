---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e127b0cb9198471d237df62bfedf8d2d57ecdca2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061561"
---
# Get-AzsStorageShareMetricDefinition

## STRESZCZENIe
Zwraca listę definicji metryk dla udziału magazynu.

## POLECENIA

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## Opis
Zwraca listę definicji metryk dla udziału magazynu.

## Przykłady

### PRZYKŁAD 1
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

Pobierz listę definicji metryk dla udziału magazynu.

## PARAMETRÓW

### -Farmname
Identyfikator farmy.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_udziału
Nazwa udziału.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
Pomijanie pierwszych N elementów określonych przez wartość parametru.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition

## INFORMACYJN

## LINKI POKREWNE
