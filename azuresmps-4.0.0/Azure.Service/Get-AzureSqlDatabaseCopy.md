---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402426"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
Sprawdza stan relacji kopiowania.

## SKŁADNIA

### ByServerNameOnly (Default)
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

## OPIS
Polecenie **cmdlet Get-AzureSqlDatabaseCopy** sprawdza stan co najmniej jednej aktywnej relacji kopiowania.
Uruchom to polecenie cmdlet po uruchomieniu Start-AzureSqlDatabaseCopy lub Stop-AzureSqlDatabaseCopy cmdlet.
Możesz sprawdzić konkretną relację kopiowania, wszystkie relacje kopiowania lub filtrowaną listę relacji kopiowania, na przykład wszystkie kopie na określonym serwerze docelowym.
To polecenie cmdlet można uruchomić na serwerze hostowym źródłową lub docelową bazę danych.

To polecenie cmdlet jest synchroniczne.
Polecenie cmdlet blokuje konsolę programu Azure PowerShell do momentu, aż zwróci obiekt stanu.

Parametry *partnerServer i* *PartnerDatabase* są opcjonalne.
Jeśli nie określisz ani jednego z parametrów, to polecenie cmdlet zwróci tabelę wyników.
Aby wyświetlić stan tylko dla konkretnej bazy danych, określ oba parametry.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie stanu kopii bazy danych
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

To polecenie pobiera stan bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.
Parametr *PartnerServer* ogranicza to polecenie do serwera bk0b8kf658.

### Przykład 2. Uzyskiwanie stanu wszystkich kopii na serwerzeUzyskanie stanu wszystkich kopii na serwerze
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

To polecenie pobiera stan wszystkich aktywnych kopii na serwerze o nazwie lpqd0zbr8y.

## PARAMETERS

### — Baza danych
Określa obiekt reprezentujący źródłową bazę danych Azure SQL Database.
To polecenie cmdlet pobiera stan kopii bazy danych, który określa ten parametr.

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
To polecenie cmdlet pobiera stan kopii bazy danych, który określa ten parametr.
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
To polecenie cmdlet pobiera stan kopii bazy danych, który określa ten parametr.

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
Jeśli ta baza danych nie zostanie znaleziona w sys.dm_database_copies zarządzania dynamicznego, to polecenie cmdlet zwraca pusty obiekt stanu.

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
Określa nazwę serwera hostowego docelową bazę danych.
Jeśli ten serwer nie zostanie znaleziony w sys.dm_database_copies zarządzania dynamicznego, to polecenie cmdlet zwraca pusty obiekt stanu.

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

### — Profil
Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.
Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.

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

### -ServerName
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## OUTPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## NOTATKI
* Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach. Aby uzyskać przykład sposobu używania uwierzytelniania opartego na certyfikatach w celu ustawienia bieżącej subskrypcji, zobacz New-AzureSqlDatabaseServerContext cmdlet.

## LINKI POKREWNE

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje na platformie Azure SQL Databases](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


