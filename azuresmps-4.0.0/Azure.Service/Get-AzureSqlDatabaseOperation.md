---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055259"
---
# Get-AzureSqlDatabaseOperation

## STRESZCZENIe
Pobiera stan operacji bazy danych na serwerze Azure.

## POLECENIA

### ByConnectionContext (domyślny)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSqlDatabaseOperation** Pobiera stan operacji bazy danych na określonym serwerze Azure.
Jeśli określisz tylko parametr *nazwa_serwera* lub *ConnectionContext* , polecenie cmdlet pobiera wszystkie operacje bazy danych dla serwera.
Jeśli określisz również bazę danych przy użyciu parametru *Database* lub *DatabaseName* , to polecenie cmdlet pobiera wszystkie operacje dla określonej bazy danych.
Jeśli określisz identyfikator GUID operacji i *nazwa_serwera* lub *ConnectionContext* , polecenie cmdlet pobiera pojedynczą operację bazy danych.

## Przykłady

### Przykład 1: uzyskiwanie stanu wszystkich operacji bazy danych dla bazy danych
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

To polecenie uzyskuje stan wszystkich operacji bazy danych w bazie danych o nazwie Database17 na serwerze, który $Context określał kontekst połączenia.

### Przykład 2: uzyskiwanie stanu wszystkich operacji bazy danych dla serwera
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

To polecenie pobiera stan wszystkich operacji bazy danych na serwerze, który $Context określał kontekst połączenia.

## PARAMETRÓW

### -ConnectionContext
Określa kontekst połączenia serwera.

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
Określa obiekt reprezentujący bazę danych SQL Azure.
W przypadku określenia tego parametru należy określić parametr *servername* lub parametr *ConnectionContext* .

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

### -DatabaseName
Określa nazwę bazy danych.
W przypadku określenia tego parametru należy określić parametr *servername* lub parametr *ConnectionContext* .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationGuid
Określa identyfikator operacji reprezentujący określoną operację bazy danych, dla której to polecenie cmdlet pobiera stan.
Identyfikatory operacji można uzyskać, żądając wszystkich operacji bazy danych usługi Azure SQL Server lub serwera.
W przypadku określenia tego parametru należy określić parametr *servername* lub parametr *ConnectionContext* .

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Nazwa_serwera
Określa nazwę serwera.

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

### Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerContext

### System. GUID

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponseList []
To polecenie cmdlet zwraca tablicę obiektów **DatabaseOperationResponseList** , jeśli zostanie wyświetlonych wiele operacji.

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponse

## INFORMACYJN

## LINKI POKREWNE

[Baza danych SQL Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Stan operacji bazy danych](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Nowe — AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


