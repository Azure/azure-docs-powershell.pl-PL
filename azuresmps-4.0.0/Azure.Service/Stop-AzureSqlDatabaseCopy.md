---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405622"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
Kończy relację kopiowania ciągłego.

## SKŁADNIA

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Stop-AzureSqlDatabaseCopy** kończy relację kopiowania ciągłego.
To polecenie cmdlet zatrzymuje ruch danych między źródłową bazą danych a pomocniczą lub docelową bazą danych, a następnie zmienia stan pomocniczej bazy danych na autonomiczną bazę danych online.

Istnieją dwa sposoby zakończenia ciągłej relacji kopiowania, zakończenia lub planowanego zakończenia oraz rozwiązania wymuszonego z możliwością utraty danych.
Na serwerze hostowym źródłową bazę danych możesz uruchomić to polecenie cmdlet w trybie zakończenia lub zakończenia wymuszonego.
Na serwerze hostowym pomocniczą bazę danych należy użyć trybu zakończenia wymuszonego.

Planowane zakończenie czeka, aż wszystkie zatwierdzone transakcje w źródłowej bazie danych (w momencie uruchamiania polecenia cmdlet) będą replikowane do pomocniczej bazy danych.
Zakończenie wymuszone nie czeka na replikację wszystkich zaległych transakcji zatwierdzonej i może spowodować utratę danych w pomocniczej bazie danych.

Gdy stan replikacji to OCZEKUJE, tylko wymuszone zakończenie może pomyślnie zakończyć relację kopiowania ciągłego.
Jeśli stan replikacji to OCZEKUJE, zakończenie, które nie jest wymuszone, nie jest obsługiwane.

## PRZYKŁADY

### Przykład 1. Zakończenie relacji kopiowania ciągłego
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

To polecenie kończy relację kopiowania ciągłego bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.
Serwer o nazwie bk0b8kf658 hostuje pomocniczą bazę danych.

### Przykład 2. Forcibly terminate a continuous copy relationship
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Pierwsze polecenie pobiera relację kopiowania bazy danych dla bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.

Drugie polecenie na stałe kończy relację kopiowania ciągłego z serwera hostowego pomocniczą bazę danych.

## PARAMETERS

### — Baza danych
Określa obiekt reprezentujący źródłową bazę danych Azure SQL Database.
To polecenie cmdlet powoduje zakończenie relacji kopii ciągłej bazy danych, która jest określana przez ten parametr.

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
To polecenie cmdlet powoduje zakończenie relacji kopii ciągłej bazy danych, która jest określana przez ten parametr.
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
Określa nazwę bazy danych.
To polecenie cmdlet powoduje zakończenie relacji kopii ciągłej bazy danych, która jest określana przez ten parametr.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.

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

### -ForcedTermination
Wskazuje, że to polecenie cmdlet powoduje wymuszone zakończenie relacji kopiowania ciągłego.
Wymuszone rozwiązanie umowy może spowodować utratę danych.
Aby uruchomić to polecenie cmdlet na serwerze hostowym docelową bazę danych, musisz określić ten parametr.
Aby uruchomić to polecenie cmdlet na serwerze hostowym źródłową bazę danych, jeśli pomocnicza baza danych jest niedostępna, musisz określić ten parametr.

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

### -PartnerDatabase
Określa nazwę pomocniczej bazy danych.
Określenie nazwy musi być zgodne z nazwą źródłowej bazy danych.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Określa nazwę serwera hostowego docelową bazę danych.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
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
Określa nazwę serwera, na którym znajduje się źródłowa baza danych.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## DANE WYJŚCIOWE

### Brak

## NOTATKI
* Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach. Aby uzyskać przykład sposobu używania uwierzytelniania opartego na certyfikatach w celu ustawienia bieżącej subskrypcji, zobacz polecenie cmdlet **New-AzureSqlDatabaseServerContext.**
* Ograniczenia: Na serwerze hostowym pomocniczą bazę danych obsługiwane jest tylko rozwiązanie wymuszone.
* Wpływ zakończenia na poprzednią pomocniczą bazę danych: Po zakończeniu pomocnicza baza danych staje się niezależną bazą danych. Jeśli baza danych została już ukończona w pomocniczej bazie danych, po zakończeniu tej bazy danych będzie ona otwarta do pełnego dostępu. Jeśli źródłową bazą danych jest baza danych do odczytu i zapisu, poprzednia pomocnicza baza danych również staje się bazą danych do odczytu i zapisu.

  Jeśli trwa iniekcjowanie, oznacza to, że iniekcjowanie zostanie przerwane, a poprzednia pomocnicza baza danych nigdy nie będzie widoczna na serwerze hostowym pomocniczej bazy danych.

* Źródłową bazę danych można ustawić jako tryb tylko do odczytu. Gwarantuje to synchronizowanie źródłowych i pomocniczych baz danych po zakończeniu oraz zapewnia, że podczas zakończenia nie są zatwierdzone żadne transakcje. Po zakończeniu zakończenia ustaw dla źródła powrót do trybu odczytu i zapisu. Opcjonalnie możesz również ustawić dla poprzedniej pomocniczej bazy danych tryb odczytu i zapisu.
* Monitorowanie: Aby sprawdzić stan operacji na poziomie źródłowym i docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation.**

## LINKI POKREWNE

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje na platformie Azure SQL Databases](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Zatrzymywanie kopiowania bazy danych](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


