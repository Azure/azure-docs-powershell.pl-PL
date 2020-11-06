---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522981"
---
# New-AzsDataDiskObject

## STRESZCZENIe
Tworzy dysk danych, który służy do tworzenia nowego obrazu platformy maszyny wirtualnej.

## POLECENIA

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## Opis
Tworzy obiekt przechowujący informacje o dysku danych.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

Utwórz nowy obiekt dysku danych.

## PARAMETRÓW

### -LUN
Numer jednostki logicznej.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Lokalizacja szablonu dysku.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

