---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054939"
---
# New-AzureSqlDatabase

## STRESZCZENIe
Tworzy bazę danych SQL Azure.

## POLECENIA

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureSqlDatabase** tworzy bazę danych SQL Azure.
Serwer można określić za pomocą kontekstu połączenia serwera bazy danych Azure SQL Server tworzonego przy użyciu polecenia cmdlet **New-AzureSqlDatabaseServerContext** .
Jeśli określisz nazwę serwera, polecenie cmdlet użyje bieżących informacji o subskrypcji platformy Azure do uwierzytelnienia żądania dostępu do serwera.

Podczas tworzenia nowej bazy danych przez określenie serwera bazy danych SQL Azure polecenie cmdlet **New-AzureSqlDatabase** tworzy tymczasowy kontekst połączenia przy użyciu określonej nazwy serwera i bieżących informacji o subskrypcji platformy Azure do wykonania tej operacji.

## Przykłady

### Przykład 1. Tworzenie bazy danych
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

To polecenie tworzy bazę danych SQL Azure o nazwie database1 dla kontekstu połączenia serwera bazy danych Azure SQL Server $Context.

### Przykład 2: Tworzenie bazy danych w bieżącej subskrypcji
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

W tym przykładzie jest tworzona baza danych o nazwie database1 w określonym serwerze bazy danych SQL Azure o nazwie lpqd0zbr8y.
Polecenie cmdlet używa bieżących informacji o subskrypcji platformy Azure do uwierzytelnienia żądania dostępu do serwera.

## PARAMETRÓW

### — Sortowanie
Określa sortowanie dla nowej bazy danych.

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

### -ConnectionContext
Określa kontekst połączenia serwera, na którym to polecenie cmdlet tworzy bazę danych.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Określa nazwę nowej bazy danych.

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

### -Edition
Określa wydanie nowej bazy danych SQL Azure.
Prawidłowe wartości: 

- Znaleziono
- Siecią
- Biznesu
- Podstawowym
- Standard
-  Ubezpieczeni

Wartość domyślna to Web.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Umożliwia wykonanie akcji bez monitowania użytkownika o potwierdzenie.

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

### -MaxSizeBytes
Określa maksymalny rozmiar bazy danych w bajtach.
Możesz określić albo ten parametr, albo parametr *MaxSizeGB* .
Zobacz opis parametru *MaxSizeGB* , aby uzyskać dopuszczalne wartości na podstawie wersji.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
Określa maksymalny rozmiar bazy danych w gigabajtach.
Możesz określić albo ten parametr, albo parametr *MaxSizeBytes* .
Dopuszczalne wartości różnią się w zależności od wersji.

Wartości podstawowego wydania: 1 lub 2

Wartości w standardzie Edition: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 lub 250

Wartości Premium Edition: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 lub 500

Wartości w sieci Web: 1 lub 5

Wartości w wersji dla firm: 10, 20, 30, 40, 50, 100 lub 150

```yaml
Type: Int32
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

### -Nazwa_serwera
Określa nazwę serwera bazy danych SQL Azure, który ma zawierać nową bazę danych.

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

### -Servicesprzeciw
Określa obiekt reprezentujący nowy cel usługi (poziom wydajności) dla tej bazy danych.
Ta wartość reprezentuje poziom zasobów przypisanych do tej bazy danych.
Prawidłowe wartości: 

Podstawowe: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 * Standard (S3): 789681b8-Ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) jest częścią najnowszej aktualizacji bazy danych SQL V12 (wersja Preview).
Aby uzyskać więcej informacji, zobacz co nowego w usłudze Azure SQL Database V12 Preview https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database

## INFORMACYJN
* Aby usunąć bazę danych utworzoną za pomocą polecenia **New-AzureSqlDatabase** , użyj polecenia cmdlet Remove-AzureSqlDatabase.

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Tworzenie bazy danych](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Nowe — AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


