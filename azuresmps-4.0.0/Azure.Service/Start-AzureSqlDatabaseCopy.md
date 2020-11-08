---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054811"
---
# Start-AzureSqlDatabaseCopy

## STRESZCZENIe
Rozpoczyna operację kopiowania bazy danych SQL Azure.

## POLECENIA

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

## Opis
Polecenie cmdlet **Start-AzureSqlDatabaseCopy** rozpoczyna jednorazową operację kopiowania lub ciągłą operację kopiowania określonej bazy danych SQL Azure.
To polecenie cmdlet nie jest transakcyjne.

Pierwotna baza danych jest źródłową bazą danych.
Kopia jest pomocniczą lub docelową bazą danych.
W przypadku ciągłej kopii bazy danych źródłowych i docelowych nie mogą znajdować się na tym samym serwerze, a serwery, które obsługują źródłową i docelową bazę danych, muszą być częścią tego samego abonamentu.

Jeśli nie określisz parametru *ContinuousCopy* , to polecenie cmdlet utworzy jednorazową kopię źródłowej bazy danych.
Po odebraniu odpowiedzi operacja może być nadal w toku.
Operację można monitorować za pomocą polecenia cmdlet Get-AzureSqlDatabaseCopy lub Get-AzureSqlDatabaseOperation.

Jeśli określisz *ContinuousCopy* , to polecenie cmdlet utworzy ciągłą kopię źródłowej bazy danych.
Po odebraniu odpowiedzi operacja będzie w toku.
Operację można monitorować, korzystając z polecenia **Get-AzureSqlDatabaseCopy** lub **Get-AzureSqlDatabaseOperation**.

Możesz utworzyć ciągłą kopię jako bazę danych w trybie online lub offline.
Nieprzerwana kopia online jest używana do konfigurowania aktywnego Geo-Replication bazy danych SQL Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
Ciągła Kopia offline jest używana do konfigurowania standardowego Geo-Replication bazy danych SQL Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## Przykłady

### Przykład 1: Planowanie ciągłej kopii bazy danych
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

To polecenie planuje ciągłą kopię bazy danych o nazwanych zamówieniach na serwerze o nazwie lpqd0zbr8y.
Polecenie utworzy docelową bazę danych na serwerze o nazwie bk0b8kf658.

### Przykład 2: Tworzenie jednorazowej kopii na tym samym serwerze
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

To polecenie umożliwia utworzenie jednorazowej kopii bazy danych o nazwanych zamówieniach na serwerze o nazwie lpqd0zbr8y.
Polecenie utworzy kopię o nazwie OrdersCopy na tym samym serwerze.

### Przykład 3: Planowanie ciągłej kopii bazy danych w trybie offline
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

To polecenie planuje ciągłą kopię bazy danych o nazwanych zamówieniach na serwerze o nazwie lpqd0zbr8y.
To polecenie tworzy docelową bazę danych w trybie offline na serwerze o nazwie bk0b8kf658.

## PARAMETRÓW

### -ContinuousCopy
Oznacza, że kopia bazy danych będzie ciągła w kopii (bazy danych repliki).
Ciągła kopia nie jest obsługiwana na tym samym serwerze.
Jeśli ten parametr nie jest określony, wykonywana jest jednorazowa kopia.
W przypadku kopii jednorazowej bazy danych źródłowych i partnerskich muszą znajdować się na tym samym serwerze.

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

### -Database
Określa obiekt reprezentujący źródłową bazę danych SQL Azure.
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

### -OfflineSecondary
Określa, że kopia ciągła jest kopią pasywną, a nie aktywną kopią.
Jeśli źródłowa baza danych jest standardową bazą danych wersji, ten parametr jest wymagany.
Jeśli ten parametr jest określony, należy również określić *ContinuousCopy* .

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
Jeśli określisz parametr *ContinuousCopy* , wartość dla *PartnerDatabase* musi być zgodna z nazwą źródłowej bazy danych.
Jeśli nie określisz *ContinuousCopy* , musisz określić nazwę docelowej bazy danych, która może różnić się od nazwy źródłowej bazy danych.

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
Określa nazwę serwera obsługującego docelową bazę danych.
Ten serwer musi znajdować się w tej samej subskrypcji platformy Azure co źródłowy serwer bazy danych.

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

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy

## INFORMACYJN
* Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach. Aby zapoznać się z przykładem używania uwierzytelniania opartego na certyfikatach do ustawiania bieżącego abonamentu, zobacz New-AzureSqlDatabaseServerContext polecenia cmdlet.
* Monitorowanie: Aby sprawdzić stan jednej lub większej liczby relacji kopii ciągłej, które są aktywne na serwerze, użyj polecenia cmdlet **Get-AzureSqlDatabaseCopy** . Aby sprawdzić stan operacji zarówno w źródle, jak i w miejscu docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation** .

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Uruchamianie kopii bazy danych](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Polecenia cmdlet usługi Azure SQL Database](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Zatrzymaj — AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


