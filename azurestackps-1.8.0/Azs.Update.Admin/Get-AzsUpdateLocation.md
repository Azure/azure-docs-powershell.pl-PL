---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889165"
---
# Get-AzsUpdateLocation

## STRESZCZENIe
Pobierz listę lokalizacji aktualizacji.

## POLECENIA

### Lista (domyślna)
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## Opis
Pobierz listę lokalizacji aktualizacji. Zwracane lokalizacje mogą być używane do uzyskiwania dostępnych aktualizacji w określonej lokalizacji za pomocą polecenia Get-AzsUpdate.

## Przykłady

### PRZYKŁAD 1
```
Get-AzsUpdateLocation
```

Pobierz listę lokalizacji aktualizacji.

## PARAMETRÓW

### — Lokalizacja
Nazwa lokalizacji.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów, w której znajduje się zasób.

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

### -ResourceId
Identyfikator zasobu.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

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

### Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation

## INFORMACYJN

## LINKI POKREWNE
