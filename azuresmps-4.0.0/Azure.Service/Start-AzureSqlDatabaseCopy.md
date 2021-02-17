---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413068"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Rozpoczyna operację kopiowania bazy danych Azure SQL Database.

## SKŁADNIA

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Start-AzureSqlDatabaseCopy** uruchamia operację kopiowania jednej lub ciągłej kopii określonej usługi Azure SQL Database.
To polecenie cmdlet nie jest transactional.

Oryginalna baza danych jest źródłową bazą danych.
Kopia jest pomocniczą lub docelową bazą danych.
W przypadku kopii ciągłej źródłowe i docelowe bazy danych nie mogą znajdować się na tym samym serwerze, a serwery hostujące źródłowe i docelowe bazy danych muszą być częścią tej samej subskrypcji.

Jeśli parametr *ContinuousCopy* nie zostanie określony, to polecenie cmdlet utworzy kopię źródłową bazy danych w czasie rzeczywistym.
Po otrzymaniu odpowiedzi operacja może być nadal w toku.
Operację można monitorować za pomocą polecenia cmdlet Get-AzureSqlDatabaseCopy lub Get-AzureSqlDatabaseOperation cmdlet.

Jeśli określisz *kopię ContinuousCopy,* to polecenie cmdlet utworzy kopię ciągłą źródłowej bazy danych.
Po otrzymaniu odpowiedzi operacja będzie w toku.
Operację można monitorować przy użyciu narzędzia **Get-AzureSqlDatabaseCopy** lub **Get-AzureSqlDatabaseOperation.**

Kopię ciągłą można utworzyć jako bazę danych w trybie online lub offline.
Kopia ciągła w trybie online służy do konfigurowania usługi Active Geo-Replication dla usługi Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ Database.
Kopia ciągła w trybie offline służy do konfigurowania standardowego Geo-Replication dla usługi Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ Database.

## PRZYKŁADY

### Przykład 1. Planowanie ciągłej kopii bazy danych
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

To polecenie pozwala zaplanować ciągłą kopię bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.
To polecenie tworzy docelową bazę danych na serwerze o nazwie bk0b8kf658.

### Przykład 2. Tworzenie kopii raz na tym samym serwerze
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

To polecenie tworzy kopię bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.
Polecenie tworzy kopię o nazwie OrdersCopy na tym samym serwerze.

### Przykład 3. Planowanie ciągłej kopii bazy danych w trybie offline
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

To polecenie pozwala zaplanować ciągłą kopię bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.
To polecenie tworzy docelową bazę danych w trybie offline na serwerze o nazwie bk0b8kf658.

## PARAMETERS

### - ContinuousCopy
Wskazuje, że kopia bazy danych będzie kopią ciągłą (repliką bazy danych).
Kopia ciągła nie jest obsługiwana na tym samym serwerze.
Jeśli ten parametr nie zostanie określony, wykonywana jest kopia raz.
W przypadku kopii razowej źródło i bazy danych partnerów muszą znajdować się na tym samym serwerze.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Baza danych
Określa obiekt reprezentujący źródłową bazę danych Azure SQL Database.
Ten parametr akceptuje dane wejściowe potoku.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Określa nazwę źródłowej bazy danych.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.

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

### -OfflineSecondary
Określa, że kopia ciągła jest kopią pasywną, a nie aktywną.
Jeśli źródłową bazą danych jest baza danych w wersji Standard, ten parametr jest wymagany.
Jeśli ten parametr jest określony, należy również określić *kopię ciągłą.*

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Określa nazwę docelowej bazy danych.
W przypadku określenia *parametru ContinuousCopy* wartość *parametru PartnerDatabase* musi być dopasowana do nazwy źródłowej bazy danych.
Jeśli nie określisz *wartości ContinuousCopy,* musisz określić nazwę docelowej bazy danych, która może różnić się od nazwy źródłowej bazy danych.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Określa nazwę serwera hostowego docelową bazę danych.
Ten serwer musi mieć tę samą subskrypcję platformy Azure, co serwer źródłowej bazy danych.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## DANE WYJŚCIOWE

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## NOTATKI
* Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach. Aby uzyskać przykład sposobu używania uwierzytelniania opartego na certyfikatach w celu skonfigurowania bieżącej subskrypcji, zobacz New-AzureSqlDatabaseServerContext cmdlet.
* Monitorowanie: Aby sprawdzić stan co najmniej jednej ciągłej relacji kopiowania, które są aktywne na serwerze, użyj polecenia cmdlet **Get-AzureSqlDatabaseCopy.** Aby sprawdzić stan operacji na poziomie źródłowym i docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation.**

## LINKI POKREWNE

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje na platformie Azure SQL Databases](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Uruchamianie kopiowania bazy danych](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


