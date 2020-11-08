---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055264"
---
# Get-AzureSqlDatabase

## STRESZCZENIe
Pobiera co najmniej jeden z baz danych.

## POLECENIA

### ByConnectionContext (domyślny)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSqlDatabase** pobiera co najmniej jedno wystąpienie bazy danych SQL Azure z serwera bazy danych SQL Azure.
Serwer można określić za pomocą kontekstu połączenia serwera bazy danych Azure SQL Server tworzonego przy użyciu polecenia cmdlet **New-AzureSqlDatabaseServerContext** .
Jeśli określisz nazwę serwera bazy danych Azure SQL Server, polecenie cmdlet używa bieżących informacji o subskrypcji platformy Azure do uwierzytelnienia żądania dostępu do serwera.

Jeśli baza danych nie zostanie określona, polecenie cmdlet **Get-AzureSqlDatabase** zwraca wszystkie bazy danych z określonego serwera.

Pobieranie restorableych baz danych:

Pobieranie restorableych baz danych przy użyciu parametru *RestorableDropped* .
Aby zwrócić wszystkie restorable porzucone bazy danych, użyj parametru *RestorableDropped* bez parametrów *DatabaseName* i *DatabaseDeletionDate*.
Aby zwrócić określoną restorable porzucona baza danych, użyj parametru *RestorableDropped* z parametrami *DatabaseName* i *DatabaseDeletionDate* .
Podczas pobierania konkretnej restorable bazy danych przy użyciu parametru *DatabaseName* należy również uwzględnić parametr *DatabaseDeletionDate* , a określona wartość *DatabaseDeletionDate* musi uwzględniać czas w milisekundach zgodnych z odpowiednią bazą danych.

Polecenie cmdlet **Get-AzureSqlDatabase** zwraca wszystkie restorable porzucone na serwerze lub jedną określoną bazę danych, która pasuje zarówno do bazy danych *DatabaseName* , jak i *DatabaseDeletionDate*.
Aby zwrócić restorable bazy danych, które spełniają inne kryteria, takie jak wszystkie restorable usunięte bazy danych o określonej nazwie, należy zwrócić wszystkie restorable usunięte bazy danych, a następnie filtrować wyniki na kliencie.

## Przykłady

### Przykład 1: pobieranie wszystkich baz danych na serwerze
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

To polecenie pobiera wszystkie bazy danych na serwerze o nazwie lpqd0zbr8y.

### Przykład 2: pobieranie wszystkich restorableych baz danych na serwerze
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

To polecenie umożliwia pobranie wszystkich restorableych baz danych na serwerze o nazwie lpqd0zbr8y.

### Przykład 3: pobieranie bazy danych z serwera określonego w kontekście połączenia
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

To polecenie pobiera bazę danych o nazwie Database01 z serwera określonego przez kontekst połączenia $Context.

### Przykład 4: przechowywanie obiektu bazy danych w zmiennej
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

To polecenie pobiera bazę danych o nazwie Database01 z serwera o nazwie lpqd0zbr8y.
Polecenie zapisuje obiekt bazy danych w zmiennej $Database 01.

### Przykład 5: pobieranie restorable porzuconej bazy danych
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

To polecenie pobiera bazę danych restorable porzuconej o nazwie Database01, która została usunięta w 11/9/2012 z serwera o nazwie lpqd0zbr8y.
To polecenie zapisuje wyniki w zmiennej $DroppedDB.

### Przykład 6: pobieranie wszystkich restorableych baz danych na serwerze i filtrowanie wyników
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

To polecenie pobiera wszystkie restorable bazy danych z serwera o nazwie lpqd0zbr8y, a następnie filtruje wyniki tylko do baz danych o nazwie ContactDB.

## PARAMETRÓW

### -ConnectionContext
Określa kontekst połączenia serwera, z którego ma zostać pobrana baza danych.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Database
Określa obiekt reprezentujący bazę danych, która jest pobierana przez to polecenie cmdlet.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
Określa datę i godzinę usunięcia.
Jeśli określisz parametr *RestorableDropped* , określ ten parametr, aby pobrać restorable porzuconej bazy danych na podstawie daty i godziny usunięcia.

Parametr *DatabaseDeletionDate* musi uwzględniać czas w milisekundach, aby był zgodny z czasem odpowiedniej bazy danych.
Określenie wartości bez milisekund powoduje, że nie można odnaleźć bazy danych.

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

### -DatabaseName
Określa nazwę bazy danych, która jest pobierana przez to polecenie cmdlet.

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
Wskazuje, że to polecenie cmdlet zwraca *RestorableDroppedDatabase* obiekty, a nie obiekty *bazy danych* .
Parametru *DatabaseDeletionDate* można użyć w celu wybrania porzuconej restorable bazy danych.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDroppedDatabase
Określa obiekt reprezentujący restorable porzuconej bazy danych, która jest pobierana przez to polecenie cmdlet.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera zawierającego bazę danych, która jest pobierana przez to polecenie cmdlet.
Polecenie cmdlet używa bieżącej subskrypcji platformy Azure do uzyskiwania dostępu do serwera.

```yaml
Type: String
Parameter Sets: ByServerName
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

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase

## WYSYŁA

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
To polecenie cmdlet zwraca obiekt *bazy danych* , jeśli nie określisz parametru *RestorableDropped* .

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
To polecenie cmdlet zwraca obiekt *RestorableDroppedDatabase* , jeśli określisz parametr *RestorableDropped* .

## INFORMACYJN

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Nowe — AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Nowe — AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


