---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055369"
---
# Stop-AzureSqlDatabaseCopy

## STRESZCZENIe
Przerywa ciągłą relację między kopiami.

## POLECENIA

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

## Opis
Polecenie cmdlet **stop-AzureSqlDatabaseCopy** przerywa ciągłą relację kopiowania.
To polecenie cmdlet zatrzymuje przepływ danych między źródłową bazą danych i pomocniczą lub docelową bazą danych, a następnie zmienia stan pomocniczej bazy danych na autonomiczną bazę danych online.

Istnieją dwa sposoby kończenia nieciągłej relacji między kopiami, zakończenie lub planowane zakończenie oraz wymuszone zakończenie z możliwością utraty danych.
Na serwerze obsługującym źródłową bazę danych możesz uruchomić to polecenie cmdlet w trybie kończenia lub wymuszonego zakończenia.
Na serwerze obsługującym pomocniczą bazę danych należy użyć trybu wymuszonego kończenia.

Planowane zakończenie nastąpi do momentu zablokowania wszystkich zatwierdzonych transakcji w źródłowej bazie danych w momencie uruchomienia polecenia cmdlet, które zostały zreplikowane do pomocniczej bazy danych.
Wymuszone zakończenie nie odczeka na replikację transakcji zatwierdzonych i może spowodować utratę danych w pomocniczej bazie danych.

Gdy stan replikacji jest OCZEKUJĄCy, tylko wymuszone zakończenie może pomyślnie zakończyć relację ciągłego kopiowania.
Jeśli stan replikacji jest OCZEKUJĄCy, zakończenie nie jest obsługiwane.

## Przykłady

### Przykład 1: kończenie ciągłej relacji kopii
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

To polecenie przerywa ciągłą relację między bazą danych o nazwanych zamówieniami na serwerze o nazwie lpqd0zbr8y.
Serwer o nazwie bk0b8kf658 obsługuje pomocniczą bazę danych.

### Przykład 2: Wymuszanie zamknięcia ciągłej relacji między kopiami
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Pierwsze polecenie uzyskuje relację kopiowania bazy danych dla bazy danych o nazwie Orders na serwerze o nazwie lpqd0zbr8y.

Drugie polecenie wymusza, że relacja ciągłej kopii z serwera obsługującego pomocniczą bazę danych jest przerywana.

## PARAMETRÓW

### -Database
Określa obiekt reprezentujący źródłową bazę danych SQL Azure.
To polecenie cmdlet powoduje zakończenie ciągłej relacji kopii bazy danych, którą określa ten parametr.

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
To polecenie cmdlet powoduje zakończenie ciągłej relacji kopii bazy danych, którą określa ten parametr.
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
To polecenie cmdlet powoduje zakończenie ciągłej relacji kopii bazy danych, którą określa ten parametr.

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

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

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
Wskazuje, że to polecenie cmdlet powoduje wymuszone zakończenie działania relacji ciągłej kopii.
Wymuszone zakończenie może spowodować utratę danych.
Aby uruchomić to polecenie cmdlet na serwerze obsługującym docelową bazę danych, należy określić ten parametr.
Aby uruchomić to polecenie cmdlet na serwerze obsługującym źródłową bazę danych, jeśli pomocnicza baza danych jest niedostępna, należy określić ten parametr.

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
Jeśli określisz nazwę, musi ona odpowiadać nazwie źródłowej bazy danych.

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
Określa nazwę serwera obsługującego docelową bazę danych.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database

## WYSYŁA

### Znaleziono

## INFORMACYJN
* Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach. Aby zapoznać się z przykładem zastosowania uwierzytelniania opartego na certyfikatach w celu skonfigurowania bieżącego abonamentu, zobacz polecenie cmdlet **New-AzureSqlDatabaseServerContext** .
* Ograniczenia: na serwerze obsługującym pomocniczą bazę danych obsługiwana jest tylko wymuszona przerwa w pracy.
* Wpływ rozwiązania na poprzednią pomocniczą bazę danych: po zakończeniu pomocnicza baza danych stanie się niezależną bazą danych. Jeśli dopełnienie zostało już ukończone w pomocniczej bazie danych, po zakończeniu tej bazy danych jest otwarta, aby uzyskać pełen dostęp. Jeśli źródłowa baza danych jest bazą danych do odczytu i zapisu, baza danych była bazą danych do odczytu i zapisu.

  Jeśli napełnianie jest obecnie w toku, wstępne umieszczanie jest przerywane, a pozostała pomocnicza baza danych nigdy nie staje się widoczna na serwerze obsługującym pomocniczą bazę danych.

* Źródłową bazę danych można ustawić w trybie tylko do odczytu. Gwarantuje to, że źródłowe i pomocnicze bazy danych są synchronizowane po zakończeniu działania, i że podczas kończenia pracy nie są zatwierdzane żadne transakcje. Po zakończeniu kończenia ustaw źródło z powrotem na tryb do odczytu i zapisu. Opcjonalnie możesz również ustawić poprzednią pomocniczą bazę danych w trybie do odczytu i zapisu.
* Monitorowanie: Aby sprawdzić stan operacji zarówno w źródle, jak i w miejscu docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation** .

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Zatrzymywanie kopiowania bazy danych](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Polecenia cmdlet usługi Azure SQL Database](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start — AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


