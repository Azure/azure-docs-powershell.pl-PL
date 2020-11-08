---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054718"
---
# Start-AzureSqlDatabaseExport

## STRESZCZENIe
Rozpoczyna operację eksportowania z bazy danych SQL Azure do magazynu obiektów BLOB.

## POLECENIA

### ByContainerObject
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByContainerName
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureSqlDatabaseExport** rozpoczyna operację eksportowania z bazy danych SQL Azure do magazynu obiektów BLOB.
Operacja wymaga kontekstu połączenia serwera bazy danych.
Użyj polecenia cmdlet Get-AzureSqlDatabaseImportExportStatus, aby uzyskać stan operacji eksportowania.

## Przykłady

### Przykład 1. Eksportowanie bazy danych
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

W tym przykładzie zainicjowano proces eksportowania z bazy danych SQL Azure zawierającej nazwę przechowywaną w zmiennej $DatabaseName do magazynu obiektów BLOB przechowywanego w zmiennej $BlobName.

## PARAMETRÓW

### -Obiekt blobname
Określa nazwę magazynu obiektów blob platformy Azure, w którym polecenie cmdlet eksportuje bazę danych.

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

### -DatabaseName
Określa nazwę bazy danych, z której to polecenie cmdlet eksportuje dane.

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

### -SqlConnectionContext
Określa kontekst połączenia serwera, który zawiera bazę danych.

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainer
Określa kontener magazynu zawierający obiekt BLOB, do którego jest eksportowany Program Database.

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerName
Określa nazwę kontenera magazynu zawierającego obiekt BLOB, do którego jest eksportowany baza danych przy użyciu tego polecenia cmdlet.

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContext
Określa kontekst kontenera magazynu obiektów BLOB.

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
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

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. ImportExportRequest

## INFORMACYJN

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Eksportowanie bazy danych](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseImportExportStatus](./Get-AzureSqlDatabaseImportExportStatus.md)

[Start — AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


