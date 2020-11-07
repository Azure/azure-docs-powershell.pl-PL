---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889061"
---
# Get-AzsComputeQuota

## STRESZCZENIe
Zwraca przydziały określające limity przydziałów dla obiektów obliczeniowych.

## POLECENIA

### Lista (domyślna)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## Opis
Zapoznaj się z listą istniejących przydziałów.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

Pobieranie wszystkich przydziałów obliczeń w określonej lokalizacji.

### --------------------------PRZYKŁAD 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Uzyskiwanie określonego przydziału obliczeń.

## PARAMETRÓW

### — Lokalizacja
{{Opis lokalizacji wypełniania}}

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

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
Position: 1
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### ComputeQuotaObject

## INFORMACYJN

## LINKI POKREWNE

