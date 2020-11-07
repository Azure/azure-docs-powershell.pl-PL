---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889054"
---
# Get-AzsDiskMigrationJob

## STRESZCZENIe
Zwraca listę zadań dotyczących migracji dysków zarządzanych.

## POLECENIA

### Lista (domyślna)
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### Pobierz
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## Opis
Zwraca listę zadań migracji dysków.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

Uzyskiwanie określonego zadania dotyczącego migracji dysków zarządzanych.

### --------------------------PRZYKŁAD 2--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local
```

Zwraca listę zadań zarządzanych migracji dysków w lokalizacji lokalnej.

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

### -Name (nazwa)
Nazwa GUID zadania migracji.

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

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
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Parametry stanu zadania migracji dysków.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. COMPUTE. admin. models. DiskMigrationJob

## INFORMACYJN

## LINKI POKREWNE

