---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523050"
---
# Get-AzsPlan

## STRESZCZENIe
Lista wszystkich planów we wszystkich abonamentach.

## POLECENIA

### ListAll (domyślny)
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### Lista
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## Opis
Lista wszystkich planów we wszystkich abonamentach.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

Pobierz plan konkretną w ramach tych abonamentów.

## PARAMETRÓW

### -Name (nazwa)
Nazwa planu.

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

### -ResourceGroupName
Nazwa grupy zasobów, w której znajduje się zasób.

```yaml
Type: String
Parameter Sets: Get, List
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
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Pomijanie pierwszych N elementów określonych przez wartość parametru.

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Początek
Zwraca N pierwszych elementów określonych przez wartość parametru.
Obowiązuje po parametrze-Skip.

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Subscriptions. admin. models. plan

## INFORMACYJN

## LINKI POKREWNE

