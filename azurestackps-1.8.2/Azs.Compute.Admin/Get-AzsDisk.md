---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055655"
---
# Get-AzsDisk

## STRESZCZENIe
Zwraca listę zarządzanych dysków, które można migrować w określonym udziale.

## POLECENIA

### Lista (domyślna)
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### Zasobów
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### Pobierz
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## Opis
Zwraca listę dysków.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
$disks = Get-AzsDisk -location local
```

Zwraca listę dysków zarządzanych w lokalizacji lokalnej.
Domyślnie będzie to pierwsze 100 dysków

### --------------------------PRZYKŁAD 2--------------------------
```
$disk = Get-AzsDisk -location local -name $DiskId
```

Uzyskiwanie określonego zarządzanego dysku.

## PARAMETRÓW

### -Count
Maksymalna liczba dysków, które mają zostać zwrócone.

```yaml
Type: Int32
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
Identyfikator GUID dysku jako tożsamość.

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

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

### -SharePath
Udział źródłowy, do którego należy zasób.

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

### -Start
Indeks początkowy dysków w zapytaniu.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Parametry stanu dysku.

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

### -UserSubscriptionId
Identyfikator subskrypcji dzierżawy, do której należy zasób.

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

### Microsoft. AzureStack. Management. COMPUTE. admin. modele. dysk

## INFORMACYJN

## LINKI POKREWNE

