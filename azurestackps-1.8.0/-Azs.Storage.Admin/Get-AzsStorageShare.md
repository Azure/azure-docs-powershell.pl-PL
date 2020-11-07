---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889105"
---
# Get-AzsStorageShare

## STRESZCZENIe
Zwraca listę udziałów w magazynie.

## POLECENIA

### Lista (domyślna)
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## Opis
Zwraca listę udziałów w magazynie.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

Pobierz listę udziałów w magazynie.

## PARAMETRÓW

### -Farmname
Identyfikator farmy.

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

### -Name (nazwa)
Nazwa udziału.

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

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

### Microsoft. AzureStack. Management. Storage. admin. models. Share

## INFORMACYJN

## LINKI POKREWNE

