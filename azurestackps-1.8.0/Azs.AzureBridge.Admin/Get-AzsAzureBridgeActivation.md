---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9374f8a55beca561afd9ed4bca4320b685349798
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/22/2020
ms.locfileid: "93899450"
---
# Get-AzsAzureBridgeActivation

## STRESZCZENIe
Zwraca aktywację mostka Azure.

## POLECENIA

### Lista (domyślna)
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### Zasobów
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## Opis
Po zarejestrowaniu stosu platformy Azure obiekt aktywacji zawiera informacje, które łączą wdrożenie stosu platformy Azure do swojej rejestracji na platformie Azure, na przykład datę wygaśnięcia rejestracji, nazwę itd.

## Przykłady

### PRZYKŁAD 1
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

Uzyskiwanie listy aktywacji usługi Azure Bridge w grupie zasobów "activationRG"

### PRZYKŁAD 2
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

Uzyskiwanie aktywacji usługi Azure Bridge na podstawie nazwy "Moja Aktywacja" znajdującej się w obszarze "activationRG"

## PARAMETRÓW

### -Name (nazwa)
Nazwa aktywacji.

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
Grupa zasobów używana podczas rejestracji stosu platformy Azure; Możesz również wyświetlić nazwy grup zasobów w portalu.

```yaml
Type: String
Parameter Sets: List, Get
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
Parameter Sets: List
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
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. AzureBridge. admin. models. ActivationResource

## INFORMACYJN

## LINKI POKREWNE
