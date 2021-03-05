---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: 7a790610d9ff3334494276eee7bb85af5b9ba3fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002705"
---
# Get-AzStorageBlobQueryResult

## SYNOPSIS
Stosuje prostą instrukcję Sql (Structured Query Language) do zawartości obiektu blob i zapisuje tylko podzbiór danych, do których został zapytany, w pliku lokalnym.

## SKŁADNIA

### NamePipeline (Default)
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BlobPipeline
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageBlobQueryResult** powoduje zastosowanie prostej instrukcji SQL (Structured Query Language) do zawartości obiektu blob i zapisanie podzbioru danych, o który zapytano, w pliku lokalnym.

## PRZYKŁADY

### Przykład 1. Kwerenda obiektu blob
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

To polecenie przekieruje obiekt blob pomyślnie z konfiguracją wejściowym jako plikiem csv i konfiguracją wyjściową jako json, a następnie zapisz dane wyjściowe w pliku lokalnym "c:\resultfile.jssię".

### Przykład 2. Tworzenie zapytania migawki obiektu blob
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

To polecenie najpierw pobiera obiekt blob dla migawki obiektów blob, a następnie wysyła zapytanie migawki obiektu blob i wyświetla wynik, w tym błąd zapytania.

## PARAMETERS

### — obiekt blob
Nazwa obiektu blob

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobBaseClient
Obiekt BlobBaseClient

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BlobContainerClient
Obiekt BlobContainerClient

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Maksymalny czas wykonywania po stronie klienta dla każdego żądania w sekundach.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Całkowita ilość jednoczesnych zadań synchronizacji.
Wartość domyślna to 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Kontener
Nazwa kontenera

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — kontekst
Obiekt kontekstowy magazynu platformy Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymuszanie
Wymusz zastąpienie istniejącego pliku.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputTextConfiguration
Konfiguracja używana do obsługi tekstu wejściowego zapytania. Utwórz obiekt konfiguracji za pomocą new-azstorageBlobQueryConfig.

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputTextConfiguration
Konfiguracja używana do obsługi tekstu wyjściowego zapytania. Utwórz obiekt konfiguracji za pomocą new-azstorageBlobQueryConfig.

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Sprawdź, czy określony obiekt blob został pomyślnie zwrócony.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryString
Ciąg zapytania, zobacz więcej szczegółów w: https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultFile
Lokalna ścieżka pliku do zapisania wyniku zapytania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Czas serwera dla każdego żądania (w sekundach).

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SnapshotTime
Migawka obiektów blob

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VersionId
Blob VersionId

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Azure.Storage.Blobs.Specialized.BlobBaseClient

### Azure.Storage.Blobs.BlobContainerClient

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI

## LINKI POKREWNE
