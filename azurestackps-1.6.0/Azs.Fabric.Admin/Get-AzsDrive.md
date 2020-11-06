---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522953"
---
# Get-AzsDrive

## STRESZCZENIe
Zwraca listę wszystkich dysków magazynu dla określonego klastra.

## POLECENIA

### Lista (domyślna)
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Pobierz
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## Opis
Zwraca listę wszystkich dysków magazynu dla określonego klastra.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

Uzyskaj listę wszystkich dysków magazynu dla określonego klastra.

### --------------------------PRZYKŁAD 2--------------------------
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

Uzyskaj dysk magazynujący według nazwy dla określonego klastra.

## PARAMETRÓW

### -Filter
Parametr filtru OData.

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

### -Name (nazwa)
Nazwa dysku magazynu.

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
Grupa zasobów, w której dostawca zasobów został zarejestrowany.

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
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleUnit
Nazwa jednostki skali.

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

### -StorageSubSystem
Podsystem magazynowania, w którym znajduje się dysk.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Fabric. admin. models. Drive
## INFORMACYJN

## LINKI POKREWNE
