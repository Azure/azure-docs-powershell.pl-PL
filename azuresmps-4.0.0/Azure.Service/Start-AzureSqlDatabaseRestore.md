---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054392"
---
# Start-AzureSqlDatabaseRestore

## STRESZCZENIe
Umożliwia wykonanie punktu przywracania bazy danych w czasie.

## POLECENIA

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureSqlDatabaseRestore** wykonuje operację przywracania czasu dla podstawowej, standardowej lub Premium bazy danych.
Baza danych SQL Azure zachowuje podstawowe kopie zapasowe baz danych — 7 dni, standard przez 14 dni i Premium dla 35 dni.
Operacja restore powoduje utworzenie nowej bazy danych.
Jeśli źródłowa baza danych nie zostanie usunięta, parametr *SourceDatabaseName* i *TargetDatabaseName* musi mieć różne wartości.

Baza danych SQL Azure nie obsługuje obecnie przywracania serwera.
Nazwy serwerów źródłowych i docelowych muszą być takie same.

## Przykłady

### Przykład 1: Przywracanie bazy danych określonej jako obiekt w momencie
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Pierwsze polecenie pobiera obiekt bazy danych dla bazy danych o nazwie Database17 na serwerze o nazwie Server01, a następnie zapisuje go w zmiennej $Database.

Drugie polecenie przywraca bazę danych do określonego momentu w określonym czasie.
Polecenie określa nazwę nowej bazy danych.

### Przykład 2: Przywracanie bazy danych określonej według nazwy do punktu w czasie
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

To polecenie przywraca bazę danych o nazwie Database17 do określonego momentu w określonej chwili.
Polecenie określa nazwę nowej bazy danych.

### Przykład 3: Przywracanie porzuconej bazy danych określonej jako obiekt do punktu w czasie
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

Pierwsze polecenie pobiera obiekt bazy danych dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.
Polecenie określa parametr *RestorableDropped* .
Z tego powodu polecenie cmdlet pobiera restorable porzucona baza danych o określonym punkcie przywracania.
Polecenie zapisuje ten obiekt bazy danych w zmiennej $Database.

Drugie polecenie przywraca porzucona bazę danych określoną przez $Database.
Polecenie określa nazwę nowej bazy danych.

## PARAMETRÓW

### -PointInTime
Określa punkt przywracania, do którego ma zostać przywrócona baza danych.
Gdy operacja przywracania zakończy się, baza danych zostanie przywrócona do stanu, w którym znajduje się na dacie i godzinie określającej ten parametr.
Domyślnie dla bazy danych na żywo, która jest obecnie ustawiona jako bieżąca godzina, a w przypadku porzuconej bazy danych, to polecenie cmdlet używa godziny porzucenia bazy danych.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDropped
Wskazuje, że to polecenie cmdlet przywraca restorable porzuconej bazy danych.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Określa nazwę bazy danych, która jest przywracana przez to polecenie cmdlet.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Określa datę i godzinę usunięcia bazy danych.
Należy uwzględnić czas w milisekundach podczas określania czasu, który będzie odpowiadał rzeczywistemu czasowi usunięcia bazy danych.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Określa nazwę bazy danych na żywo, która jest przywracana przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Określa obiekt reprezentujący restorable porzuconej bazy danych, która jest przywracana przez to polecenie cmdlet.
Aby uzyskać obiekt **RestorableDroppedDatabase** , użyj polecenia cmdlet Get-AzureSqlDatabase, a następnie określ parametr *RestorableDropped* .

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Określa nazwę serwera, na którym jest uruchomiona źródłowa baza danych, lub w której uruchomiono źródłową bazę danych przed jej usunięciem.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Określa nazwę nowej bazy danych, którą ma utworzyć operacja przywracania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Określa nazwę serwera, na którym jest przywracana baza danych.

Baza danych SQL Azure nie obsługuje obecnie przywracania serwera.
Nazwy serwerów źródłowych i docelowych muszą być takie same.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. RestoreDatabaseOperation

## INFORMACYJN
* Aby uruchomić to polecenie cmdlet, należy użyć uwierzytelniania opartego na certyfikatach. Uruchom następujące polecenia na komputerze, na którym Uruchom to polecenie cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Żądanie utworzenia bazy danych](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


