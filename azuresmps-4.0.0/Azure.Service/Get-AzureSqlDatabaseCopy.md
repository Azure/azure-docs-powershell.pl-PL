---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055261"
---
# Get-AzureSqlDatabaseCopy

## STRESZCZENIe
Sprawdza stan relacji kopiowania.

## POLECENIA

### ByServerNameOnly (domyślny)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSqlDatabaseCopy** sprawdza stan jednej lub większej liczby aktywnych relacji między kopiami.
Uruchom to polecenie cmdlet po uruchomieniu Start-AzureSqlDatabaseCopy lub Stop-AzureSqlDatabaseCopy polecenia cmdlet.
Możesz sprawdzić określoną relację kopiowania, wszystkie relacje kopiowania lub przefiltrowaną listę relacji kopiowania, takich jak wszystkie kopie na określonym serwerze docelowym.
To polecenie cmdlet można uruchomić na serwerze obsługującym źródłową lub docelową bazę danych.

To polecenie cmdlet jest synchroniczne.
Polecenie cmdlet blokuje konsolę programu Azure PowerShell do momentu, gdy zwróci ona obiekt status.

Parametry *PartnerServer* i *PartnerDatabase* są opcjonalne.
Jeśli nie określisz żadnego z parametrów, to polecenie cmdlet zwróci tabelę wyników.
Aby wyświetlić stan tylko określonej bazy danych, należy określić oba parametry.

## Przykłady

### Przykład 1. Pobieranie stanu kopii bazy danych
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

To polecenie uzyskuje stan bazy danych nazwane zamówienia na serwerze o nazwie lpqd0zbr8y.
Parametr *PartnerServer* ogranicza to polecenie do serwera bk0b8kf658.

### Przykład 2: pobieranie stanu wszystkich kopii w serverGet stan wszystkich kopii na serwerze
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

To polecenie uzyskuje stan wszystkich aktywnych kopii na serwerze o nazwie lpqd0zbr8y.

## PARAMETRÓW

### -Database
Określa obiekt reprezentujący źródłową bazę danych SQL Azure.
To polecenie cmdlet pobiera stan kopii bazy danych, którą określa ten parametr.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Określa obiekt reprezentujący bazę danych.
To polecenie cmdlet pobiera stan kopii bazy danych, którą określa ten parametr.
Ten parametr akceptuje dane wejściowe potoku.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Określa nazwę źródłowej bazy danych.
To polecenie cmdlet umożliwia pobieranie statusu kopii bazy danych, którą określa ten parametr.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Określa nazwę pomocniczej bazy danych.
Jeśli nie można odnaleźć tej bazy danych w dynamicznym widoku zarządzania sys.dm_database_copies, to polecenie cmdlet zwróci pusty obiekt status.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Określa nazwę serwera obsługującego docelową bazę danych.
Jeśli nie odnaleziono tego serwera w dynamicznym widoku zarządzania sys.dm_database_copies, to polecenie cmdlet zwróci pusty obiekt status.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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

### -Nazwa_serwera
Określa nazwę serwera, na którym znajduje się kopia bazy danych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy

## INFORMACYJN
* Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach. Aby zapoznać się z przykładem używania uwierzytelniania opartego na certyfikatach do ustawiania bieżącej subskrypcji, zobacz polecenie cmdlet New-AzureSqlDatabaseServerContext.

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Polecenia cmdlet usługi Azure SQL Database](./Azure.SQLDatabase.md)

[Start — AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Zatrzymaj — AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


