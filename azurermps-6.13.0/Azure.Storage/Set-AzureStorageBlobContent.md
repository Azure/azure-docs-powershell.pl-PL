---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: edc2a178ac8fa1c3a009830decb62d60ece2a367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542080"
---
# Set-AzureStorageBlobContent

## STRESZCZENIe
Wysyła plik lokalny do obiektu BLOB usługi Azure Storage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SendManual (domyślny)
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ContainerPipeline
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BlobPipeline
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazywanie pliku lokalnego do obiektu BLOB usługi Azure Storage.

## Przykłady

### Przykład 1: przekazywanie nazwanego pliku
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

To polecenie przekazuje plik o nazwie PlanningData do obiektu BLOB o nazwie Planning2015.

### Przykład 2: przekazywanie wszystkich plików w folderze bieżącym
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem do pobierania wszystkich plików w bieżącym folderze i podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazanie plików do kontenera o nazwie ContosoUploads.

### Przykład 3: zastąpienie istniejącego obiektu BLOB
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

To polecenie uzyskuje obiekt BLOB o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzureStorageBlob, a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.
Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.
To polecenie nie określa parametru *Force* .
Polecenie wyświetli monit o potwierdzenie.
Jeśli potwierdzisz polecenie, polecenie cmdlet zastąpi istniejący obiekt BLOB.

### Przykład 4: przekazywanie pliku do kontenera przy użyciu rurociągu
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

To polecenie uzyskuje kontener, który zaczyna się od ciągu ContosoUpload, przy użyciu polecenia cmdlet **Get-AzureStorageContainer** , a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.
Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.

### Przykład 5: przekazywanie pliku do obiektu BLOB strony za pomocą metadanych i PremiumPageBlobTier jako P10
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

Pierwsze polecenie tworzy tabelę skrótów zawierającą metadane dla obiektu BLOB i zapisuje tę tabelę w zmiennej $Metadata.
Drugie polecenie przekazuje plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.
Obiekt BLOB zawiera metadane przechowywane w $Metadata i ma PremiumPageBlobTier jako P10.

### Przykład 6: przekazywanie pliku do obiektu BLOB przy użyciu określonych właściwości obiektu BLOB
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

To polecenie wysyła plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads z określonymi właściwościami obiektu BLOB.

## PARAMETRÓW

### -Obiekt BLOB
Określa nazwę obiektu BLOB.
To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB usługi Azure Storage, który określa ten parametr.

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Blobtype
Określa typ obiektu BLOB, który jest wysyłany przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:
- Drukowany
- Strona wartość domyślna to Block.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.
Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.

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

### -CloudBlob
Określa obiekt **CloudBlob** .
Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.
To polecenie cmdlet umożliwia przekazywanie zawartości do obiektu BLOB w kontenerze, który ten parametr określa.
Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzureStorageContainer.

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Określa maksymalną liczbę współbieżnych połączeń sieciowych.
Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.
Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.
Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
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

### -Kontener
Określa nazwę kontenera.
To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB w kontenerze, który ten parametr określa.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Określa kontekst usługi Azure Storage.
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.
Aby użyć kontekstu magazynu utworzonego na podstawie tokenu SAS bez uprawnienia do odczytu, należy dodać parametr Force, aby pominąć obiekt BLOB Check.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -File (plik)
Określa lokalną ścieżkę do pliku, który ma zostać przekazany jako zawartość obiektu BLOB.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB bez monitowania o potwierdzenie.

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

### -Metadata
Określa metadane przekazanego obiektu BLOB.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PremiumPageBlobTier
Warstwa obiektu BLOB strony

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Properties
Określa właściwości przekazanego obiektu BLOB. Obsługiwane właściwości to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.
Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

### Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer

### Microsoft. platformy windowsazure. Storage. blob. CloudBlob

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)
