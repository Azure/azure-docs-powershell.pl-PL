---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710750"
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
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## Opis
Pobierz listę lokalizacji aktualizacji. Zwracane lokalizacje mogą być używane do uzyskiwania dostępnych aktualizacji w określonej lokalizacji za pomocą polecenia Get-AzsUpdate.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsUpdateLocation
```

Pobierz listę lokalizacji aktualizacji.

## PARAMETRÓW

### -Name (nazwa)
Nazwa lokalizacji aktualizacji.

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation

## INFORMACYJN

## LINKI POKREWNE

