---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055525"
---
# Get-AzureSqlRecoverableDatabase

## STRESZCZENIe
Pobiera odzyskiwalne bazy danych z określonego serwera.

## POLECENIA

### AllDatabasesOnGivenServer (domyślny)
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GivenDatabaseOnGivenServer
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### GivenDatabaseObject
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSqlRecoverableDatabase** pobiera odzyskiwalne bazy danych z określonego serwera.
To polecenie cmdlet pobiera określoną odzyskiwalną bazę danych lub wszystkie odzyskiwalne bazy danych na serwerze.

## Przykłady

### Przykład 1: pobieranie wszystkich odzyskiwalnych baz danych
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

To polecenie umożliwia pobieranie wszystkich odzyskiwalnych baz danych na serwerze o nazwie Server01.

### Przykład 2: uzyskiwanie określonej odzyskiwalnej bazy danych
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

To polecenie pobiera bazę danych o nazwie Database17 na serwerze o nazwie Server01.

## PARAMETRÓW

### -Database
Określa obiekt reprezentujący odzyskiwalną bazę danych, która jest pobierana przez to polecenie cmdlet.

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Określa nazwę odzyskiwalnej bazy danych, która ma być pobierana przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
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
Określa nazwę serwera, za pomocą którego ten aplet polecenia pobiera odzyskiwalne bazy danych.

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
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

### IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## INFORMACYJN
* Aby uruchomić to polecenie cmdlet, należy użyć uwierzytelniania opartego na certyfikatach. Uruchom następujące polecenia na komputerze, na którym Uruchom to polecenie cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Uzyskiwanie odzyskiwalnej bazy danych](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start — AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


