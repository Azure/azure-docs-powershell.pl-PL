---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054389"
---
# Start-AzureSqlDatabaseRecovery

## STRESZCZENIe
Inicjuje żądanie przywrócenia bazy danych.

## POLECENIA

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureSqlDatabaseRecovery** inicjuje żądanie przywrócenia bazy danych na żywo lub porzuconej.
To polecenie cmdlet obsługuje odzyskiwanie podstawowe, które wykorzystuje ostatnią znaną dostępną kopię zapasową bazy danych.
Operacja odzyskiwania powoduje utworzenie nowej bazy danych.
Jeśli odzyskasz bazę danych na tym samym serwerze, musisz określić inną nazwę dla nowej bazy danych.

Aby wykonać przywracanie w czasie dla bazy danych, zamiast tego użyj polecenia cmdlet **Start-AzureSqlDatabaseRestore** .

## Przykłady

### Przykład 1: odzyskiwanie bazy danych określonej jako obiekt
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

Pierwsze polecenie pobiera obiekt bazy danych przy użyciu polecenia cmdlet **Get-AzureSqlRecoverableDatabase** .
Polecenie zapisuje ten obiekt w zmiennej $Database.

Drugie polecenie odkryje bazę danych przechowywaną w $Database.

### Przykład 2: odzyskiwanie bazy danych określonej według nazwy
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

To polecenie umożliwia odkrycie bazy danych przy użyciu nazwy bazy danych.

## PARAMETRÓW

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

### -SourceDatabase
Określa obiekt bazy danych reprezentujący bazę danych, której dotyczy ten aplet polecenia.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Określa nazwę bazy danych, która ma być odzyskana przez ten aplet polecenia.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Określa nazwę serwera, na którym jest uruchomiona źródłowa baza danych, lub w której uruchomiono źródłową bazę danych przed jej usunięciem.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Określa nazwę odzyskanej bazy danych.
Jeśli źródłowa baza danych jest wciąż na żywo, w celu odzyskania jej na tym samym serwerze musisz określić nazwę, która różni się od nazwy źródłowej bazy danych.

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

### -TargetServerName
Określa nazwę serwera, na którym ma zostać przywrócona baza danych.
Bazę danych można przywrócić na tym samym serwerze lub na innym serwerze.

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

### Microsoft. platformy windowsazure. Management. SQL. MODELES. RecoverableDatabase

## WYSYŁA

### Microsoft. platformy windowsazure. Management. SQL. MODELES. RecoverDatabaseOperation

## INFORMACYJN
* Aby uruchomić to polecenie cmdlet, należy użyć uwierzytelniania opartego na certyfikatach. Uruchom następujące polecenia na komputerze, na którym jest uruchamiane to polecenie cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Utwórz żądanie odzyskania bazy danych](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Replikowanie Geo w bazie danych SQL Azure](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[Start — AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


