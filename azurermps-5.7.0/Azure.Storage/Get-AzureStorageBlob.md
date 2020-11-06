---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
ms.openlocfilehash: da3b5f969bfa8beafab20f256df237588ed87048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527173"
---
# Get-AzureStorageBlob

## STRESZCZENIe
Zawiera listę obiektów BLOB w kontenerze.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Obiekt blobname (domyślnie)
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorageBlob** zawiera listę obiektów BLOB w określonym kontenerze na koncie usługi Azure Storage.

## Przykłady

### Przykład 1: uzyskiwanie obiektu BLOB według nazwy obiektu BLOB
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

W tym poleceniu jest używana nazwa obiektu BLOB i symbol wieloznaczny w celu uzyskania obiektu BLOB.

### Przykład 2: uzyskiwanie obiektów BLOB w kontenerze przy użyciu rurociągu
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False      
```

To polecenie używa potoku, aby uzyskać wszystkie obiekty blob (w kontenerze Uwzględniaj obiekty blob w stanie usunięte).

### Przykład 3: pobieranie obiektów BLOB według prefiksu nazwy
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

To polecenie używa prefiksu nazwy w celu uzyskania dostępu do obiektów BLOB.

### Przykład 4: Wyświetlanie listy obiektów BLOB w wielu partiach
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

W tym przykładzie użyto parametrów *MaxCount* i *ContinuationToken* , aby wyświetlić obiekty blob magazynu platformy Azure w wielu partiach.
Pierwsze cztery polecenia umożliwiają przypisanie wartości do zmiennych w przykładzie.

Piąte polecenie **określa instrukcję do wykonania,** która używa polecenia cmdlet **Get-AzureStorageBlob** w celu uzyskania dostępu do obiektów BLOB.
Instrukcja zawiera token kontynuacji przechowywany w zmiennej $Token.
$Token zmienia się w trakcie uruchamiania pętli.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help About_Do` .

W poleceniu ostatnim użyto polecenia **echo** do wyświetlenia sumy.

## PARAMETRÓW

### -Obiekt BLOB
Określa nazwę lub wzorzec nazwy, który może być wykorzystywany do wyszukiwania symboli wieloznacznych.
Jeśli nie podano nazwy obiektu BLOB, polecenie cmdlet wyświetla wszystkie obiekty blob w określonym kontenerze.
Jeśli wartość jest określona dla tego parametru, polecenie cmdlet wyświetla wszystkie obiekty blob z nazwami zgodnymi z tym parametrem.

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ClientTimeoutPerRequest
Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.
Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.

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

### -ConcurrentTaskCount
Określa maksymalną liczbę współbieżnych połączeń sieciowych.
Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.
Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.
Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
Wartość domyślna to 10.

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

### -Kontener
Określa nazwę kontenera.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Określa konto usługi Azure Storage, z którego chcesz uzyskać listę obiektów BLOB.
Aby utworzyć kontekst miejsca do magazynowania, możesz użyć polecenia cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContinuationToken
Określa token kontynuacji listy obiektów BLOB.
Ten parametr oraz parametr *MaxCount* umożliwiają wyświetlanie listy obiektów BLOB w wielu partiach.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDeleted
Dołączanie do usuniętego obiektu BLOB, domyślnie polecenie Pobierz obiekt BLOB nie uwzględnia usuniętego obiektu BLOB.

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

### -MaxCount
Określa maksymalną liczbę obiektów, które zostanie zwrócone przez to polecenie cmdlet.

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

### -Prefix
Określa prefiks nazw obiektów blob, które należy uzyskać.
Ten parametr nie obsługuje wyszukiwania za pomocą wyrażeń regularnych ani symboli wieloznacznych.
Oznacza to, że jeśli kontener zawiera tylko obiekty blob o nazwie "my", "MyBlob1" i "MyBlob2", a użytkownik określi "-prefix *", polecenie cmdlet nie zwraca żadnych obiektów BLOB.
Jednak w przypadku określenia "-prefix my" polecenie cmdlet zwraca ciąg "my", "MyBlob1" i "MyBlob2".

```yaml
Type: String
Parameter Sets: BlobPrefix
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
Type: Int32
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

### IStorageContext
Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku

## WYSYŁA

### AzureStorageBlob

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)

[Set-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)


