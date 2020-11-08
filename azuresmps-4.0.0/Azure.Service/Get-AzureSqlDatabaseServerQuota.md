---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054536"
---
# Get-AzureSqlDatabaseServerQuota

## STRESZCZENIe
Pobiera informacje o przydziałach dla serwera bazy danych Azure SQL.

## POLECENIA

### ByConnectionContext
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSqlDatabaseServerQuota** pobiera informacje o przydziałach dla określonego wystąpienia serwera bazy danych SQL Azure.
Określ kontekst połączenia lub nazwę serwera.
Jeśli nie określisz nazwy przydziału, to polecenie cmdlet otrzyma wszystkie informacje o przydziałach dla serwera.

## Przykłady

### Przykład 1: uzyskiwanie informacji dotyczących określonego przydziału
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

To polecenie pobiera przydział o nazwie Premium_Databases z serwera bazy danych SQL Azure określonego przez połączenie przechowywane w zmiennej $Context.

### Przykład 2: uzyskiwanie informacji o wszystkich przydziałach
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

To polecenie pobiera wszystkie wartości przydziałów z serwera określonego przez $Context połączenia.

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

### -Przydział
Określa nazwę wartości przydziału pobieranej przez to polecenie cmdlet.

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

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. ServerQuota []

## INFORMACYJN
* Uwierzytelnianie: to polecenie cmdlet może używać uwierzytelniania programu SQL Server lub uwierzytelniania opartego na certyfikacie. Aby zapoznać się z przykładami konfigurowania uwierzytelniania, zobacz polecenie cmdlet New-AzureSqlDatabaseServerContext.

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Nowe — AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


