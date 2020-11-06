---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b30ae24d384667aa8d399f03c76ab886b2faa1c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523282"
---
# New-DataDiskObject

## STRESZCZENIe
Tworzy dysk danych, który służy do tworzenia nowego obrazu platformy maszyny wirtualnej.

## POLECENIA

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## Opis
Tworzy obiekt przechowujący informacje o dysku danych.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
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

