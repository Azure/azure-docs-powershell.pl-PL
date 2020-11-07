---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
ms.openlocfilehash: f3a88aa20c424549f074415615efe7f8190782a2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898605"
---
# <span data-ttu-id="1f50a-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1f50a-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="1f50a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f50a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f50a-103">Zawiera listę obiektów BLOB w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="1f50a-103">Lists blobs in a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f50a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f50a-104">SYNTAX</span></span>

### <span data-ttu-id="1f50a-105">Obiekt blobname (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1f50a-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f50a-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="1f50a-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f50a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1f50a-107">DESCRIPTION</span></span>
<span data-ttu-id="1f50a-108">Polecenie cmdlet **Get-AzureStorageBlob** zawiera listę obiektów BLOB w określonym kontenerze na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1f50a-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="1f50a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f50a-109">EXAMPLES</span></span>

### <span data-ttu-id="1f50a-110">Przykład 1: uzyskiwanie obiektu BLOB według nazwy obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="1f50a-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="1f50a-111">W tym poleceniu jest używana nazwa obiektu BLOB i symbol wieloznaczny w celu uzyskania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f50a-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="1f50a-112">Przykład 2: uzyskiwanie obiektów BLOB w kontenerze przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="1f50a-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="1f50a-113">To polecenie używa potoku, aby uzyskać wszystkie obiekty blob (w kontenerze Uwzględniaj obiekty blob w stanie usunięte).</span><span class="sxs-lookup"><span data-stu-id="1f50a-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="1f50a-114">Przykład 3: pobieranie obiektów BLOB według prefiksu nazwy</span><span class="sxs-lookup"><span data-stu-id="1f50a-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="1f50a-115">To polecenie używa prefiksu nazwy w celu uzyskania dostępu do obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f50a-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="1f50a-116">Przykład 4: Wyświetlanie listy obiektów BLOB w wielu partiach</span><span class="sxs-lookup"><span data-stu-id="1f50a-116">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="1f50a-117">W tym przykładzie użyto parametrów *MaxCount* i *ContinuationToken* , aby wyświetlić obiekty blob magazynu platformy Azure w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="1f50a-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="1f50a-118">Pierwsze cztery polecenia umożliwiają przypisanie wartości do zmiennych w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="1f50a-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="1f50a-119">Piąte polecenie **określa instrukcję do wykonania,** która używa polecenia cmdlet **Get-AzureStorageBlob** w celu uzyskania dostępu do obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f50a-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="1f50a-120">Instrukcja zawiera token kontynuacji przechowywany w zmiennej $Token.</span><span class="sxs-lookup"><span data-stu-id="1f50a-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="1f50a-121">$Token zmienia się w trakcie uruchamiania pętli.</span><span class="sxs-lookup"><span data-stu-id="1f50a-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="1f50a-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="1f50a-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="1f50a-123">W poleceniu ostatnim użyto polecenia **echo** do wyświetlenia sumy.</span><span class="sxs-lookup"><span data-stu-id="1f50a-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="1f50a-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f50a-124">PARAMETERS</span></span>

### <span data-ttu-id="1f50a-125">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="1f50a-125">-Blob</span></span>
<span data-ttu-id="1f50a-126">Określa nazwę lub wzorzec nazwy, który może być wykorzystywany do wyszukiwania symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="1f50a-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="1f50a-127">Jeśli nie podano nazwy obiektu BLOB, polecenie cmdlet wyświetla wszystkie obiekty blob w określonym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="1f50a-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="1f50a-128">Jeśli wartość jest określona dla tego parametru, polecenie cmdlet wyświetla wszystkie obiekty blob z nazwami zgodnymi z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="1f50a-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f50a-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f50a-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1f50a-130">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="1f50a-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1f50a-131">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="1f50a-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1f50a-132">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="1f50a-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1f50a-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1f50a-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1f50a-134">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1f50a-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1f50a-135">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1f50a-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1f50a-136">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="1f50a-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1f50a-137">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="1f50a-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1f50a-138">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="1f50a-138">The default value is 10.</span></span>

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

### <span data-ttu-id="1f50a-139">-Kontener</span><span class="sxs-lookup"><span data-stu-id="1f50a-139">-Container</span></span>
<span data-ttu-id="1f50a-140">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="1f50a-140">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f50a-141">-Context</span><span class="sxs-lookup"><span data-stu-id="1f50a-141">-Context</span></span>
<span data-ttu-id="1f50a-142">Określa konto usługi Azure Storage, z którego chcesz uzyskać listę obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f50a-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="1f50a-143">Aby utworzyć kontekst miejsca do magazynowania, możesz użyć polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1f50a-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="1f50a-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="1f50a-144">-ContinuationToken</span></span>
<span data-ttu-id="1f50a-145">Określa token kontynuacji listy obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f50a-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="1f50a-146">Ten parametr oraz parametr *MaxCount* umożliwiają wyświetlanie listy obiektów BLOB w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="1f50a-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f50a-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f50a-147">-DefaultProfile</span></span>
<span data-ttu-id="1f50a-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f50a-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f50a-149">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="1f50a-149">-IncludeDeleted</span></span>
<span data-ttu-id="1f50a-150">Dołączanie do usuniętego obiektu BLOB, domyślnie polecenie Pobierz obiekt BLOB nie uwzględnia usuniętego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f50a-150">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="1f50a-151">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1f50a-151">-MaxCount</span></span>
<span data-ttu-id="1f50a-152">Określa maksymalną liczbę obiektów, które zostanie zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f50a-152">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="1f50a-153">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1f50a-153">-Prefix</span></span>
<span data-ttu-id="1f50a-154">Określa prefiks nazw obiektów blob, które należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="1f50a-154">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="1f50a-155">Ten parametr nie obsługuje wyszukiwania za pomocą wyrażeń regularnych ani symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="1f50a-155">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="1f50a-156">Oznacza to, że jeśli kontener zawiera tylko obiekty blob o nazwie "my", "MyBlob1" i "MyBlob2", a użytkownik określi "-prefix \*", polecenie cmdlet nie zwraca żadnych obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f50a-156">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="1f50a-157">Jednak w przypadku określenia "-prefix my" polecenie cmdlet zwraca ciąg "my", "MyBlob1" i "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="1f50a-157">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f50a-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f50a-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1f50a-159">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="1f50a-159">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1f50a-160">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="1f50a-160">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1f50a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f50a-161">CommonParameters</span></span>
<span data-ttu-id="1f50a-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f50a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f50a-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f50a-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f50a-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f50a-164">INPUTS</span></span>

### <span data-ttu-id="1f50a-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1f50a-165">System.String</span></span>

### <span data-ttu-id="1f50a-166">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f50a-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1f50a-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f50a-167">OUTPUTS</span></span>

### <span data-ttu-id="1f50a-168">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1f50a-168">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="1f50a-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f50a-169">NOTES</span></span>

## <span data-ttu-id="1f50a-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f50a-170">RELATED LINKS</span></span>

[<span data-ttu-id="1f50a-171">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1f50a-171">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="1f50a-172">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1f50a-172">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="1f50a-173">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1f50a-173">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


