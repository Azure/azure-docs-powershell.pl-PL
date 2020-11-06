---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523389"
---
# Get-AzsVMExtension

## STRESZCZENIe
Zwraca dostępne obecnie rozszerzenia obrazu maszyny wirtualnej.

## POLECENIA

### Lista (domyślna)
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### Zasobów
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## Opis
Zwraca rozszerzenia obrazu maszyny wirtualnej.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsVMExtension
```

Uzyskaj wszystkie rozszerzenia maszyny wirtualnej w lokalizacji.

### --------------------------PRZYKŁAD 2--------------------------
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

Pobierz określone rozszerzenie maszyny wirtualnej.

## PARAMETRÓW

### — Lokalizacja
Lokalizacja zasobu.

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

### — Wydawca
Nazwa wydawcy.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Type
Typ rozszerzenia.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Version
Wersja rozszerzenia obrazu maszyny wirtualnej.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### VmExtensionObject

## INFORMACYJN

## LINKI POKREWNE

