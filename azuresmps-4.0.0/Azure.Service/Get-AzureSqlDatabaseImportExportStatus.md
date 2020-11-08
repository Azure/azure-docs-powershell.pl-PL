---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055260"
---
# Get-AzureSqlDatabaseImportExportStatus

## STRESZCZENIe
Pobiera stan żądania importu lub eksportu.

## POLECENIA

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSqlDatabaseImportExportStatus** Pobiera stan żądania importu lub eksportu.
Polecenie cmdlet Start-AzureSqlDatabaseImport lub Start-AzureSqlDatabaseExport inicjuje żądania.
Obiekt request można określić przy użyciu parametru *Request* lub można go zidentyfikować przy użyciu parametru *IdentyfikatorŻądania* oraz parametrów *username* , *Password* i *nazwa_serwera* .

## Przykłady

### Przykład 1: uzyskiwanie statusu żądania eksportu
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

Pierwsze polecenie tworzy żądanie eksportu, a następnie zapisuje je w zmiennej $ExportRequest.

Drugie polecenie uzyskuje stan żądania eksportu przechowywanego w $ExportRequest.

## PARAMETRÓW

### -Password (hasło)
Określa hasło wymagane do nawiązania połączenia z serwerem bazy danych SQL Azure.
Jeśli określono parametr *numer_id_żądania* , należy określić ten parametr.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### -Request
Określa obiekt **ImportExportRequest** .
Aby uzyskać obiekt request importu lub eksportu, użyj polecenia cmdlet Start-AzureSqlDatabaseImport lub Start-AzureSqlDatabaseExport.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentyfikatorŻądania
Określa identyfikator GUID operacji importu lub eksportu, dla którego to polecenie cmdlet pobiera stan.
W przypadku określenia tego parametru należy określić parametry *username* , *Password* i *nazwa_serwera* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera bazy danych SQL Azure.
Jeśli określono parametr *numer_id_żądania* , należy określić ten parametr.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Określa nazwę użytkownika wymaganą do nawiązania połączenia z serwerem bazy danych SQL Azure.
Jeśli określono parametr *numer_id_żądania* , należy określić ten parametr.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. ImportExport. StatusInfo

## INFORMACYJN

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Uzyskiwanie statusu bazy danych importowania eksportu](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start — AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[Start — AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


