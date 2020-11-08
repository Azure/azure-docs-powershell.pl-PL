---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 9f4c20c29012609c773d176fb2f80c585bd9a851
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050210"
---
# <span data-ttu-id="63154-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="63154-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="63154-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63154-102">SYNOPSIS</span></span>
<span data-ttu-id="63154-103">Zawiera listę obiektów BLOB w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="63154-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="63154-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63154-104">SYNTAX</span></span>

### <span data-ttu-id="63154-105">Obiekt blobname (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="63154-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="63154-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="63154-106">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="63154-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63154-107">DESCRIPTION</span></span>
<span data-ttu-id="63154-108">Polecenie cmdlet **Get-AzStorageBlob** zawiera listę obiektów BLOB w określonym kontenerze na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="63154-108">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="63154-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63154-109">EXAMPLES</span></span>

### <span data-ttu-id="63154-110">Przykład 1: uzyskiwanie obiektu BLOB według nazwy obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="63154-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="63154-111">W tym poleceniu jest używana nazwa obiektu BLOB i symbol wieloznaczny w celu uzyskania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="63154-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="63154-112">Przykład 2: uzyskiwanie obiektów BLOB w kontenerze przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="63154-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="63154-113">To polecenie używa potoku, aby uzyskać wszystkie obiekty blob (w kontenerze Uwzględniaj obiekty blob w stanie usunięte).</span><span class="sxs-lookup"><span data-stu-id="63154-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="63154-114">Przykład 3: pobieranie obiektów BLOB według prefiksu nazwy</span><span class="sxs-lookup"><span data-stu-id="63154-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="63154-115">To polecenie używa prefiksu nazwy w celu uzyskania dostępu do obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="63154-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="63154-116">Przykład 4: Wyświetlanie listy obiektów BLOB w wielu partiach</span><span class="sxs-lookup"><span data-stu-id="63154-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="63154-117">W tym przykładzie użyto parametrów *MaxCount* i *ContinuationToken* , aby wyświetlić obiekty blob magazynu platformy Azure w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="63154-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="63154-118">Pierwsze cztery polecenia umożliwiają przypisanie wartości do zmiennych w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="63154-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="63154-119">Piąte polecenie **określa instrukcję do wykonania,** która używa polecenia cmdlet **Get-AzStorageBlob** w celu uzyskania dostępu do obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="63154-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="63154-120">Instrukcja zawiera token kontynuacji przechowywany w zmiennej $Token.</span><span class="sxs-lookup"><span data-stu-id="63154-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="63154-121">$Token zmienia się w trakcie uruchamiania pętli.</span><span class="sxs-lookup"><span data-stu-id="63154-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="63154-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="63154-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="63154-123">W poleceniu ostatnim użyto polecenia **echo** do wyświetlenia sumy.</span><span class="sxs-lookup"><span data-stu-id="63154-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="63154-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63154-124">PARAMETERS</span></span>

### <span data-ttu-id="63154-125">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="63154-125">-Blob</span></span>
<span data-ttu-id="63154-126">Określa nazwę lub wzorzec nazwy, który może być wykorzystywany do wyszukiwania symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="63154-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="63154-127">Jeśli nie podano nazwy obiektu BLOB, polecenie cmdlet wyświetla wszystkie obiekty blob w określonym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="63154-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="63154-128">Jeśli wartość jest określona dla tego parametru, polecenie cmdlet wyświetla wszystkie obiekty blob z nazwami zgodnymi z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="63154-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="63154-129">Ten parametr obsługuje symbole wieloznaczne w dowolnym miejscu ciągu.</span><span class="sxs-lookup"><span data-stu-id="63154-129">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="63154-130">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63154-130">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="63154-131">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="63154-131">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="63154-132">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="63154-132">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="63154-133">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="63154-133">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="63154-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="63154-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="63154-135">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="63154-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="63154-136">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="63154-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="63154-137">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="63154-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="63154-138">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="63154-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="63154-139">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="63154-139">The default value is 10.</span></span>

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

### <span data-ttu-id="63154-140">-Kontener</span><span class="sxs-lookup"><span data-stu-id="63154-140">-Container</span></span>
<span data-ttu-id="63154-141">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="63154-141">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="63154-142">-Context</span><span class="sxs-lookup"><span data-stu-id="63154-142">-Context</span></span>
<span data-ttu-id="63154-143">Określa konto usługi Azure Storage, z którego chcesz uzyskać listę obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="63154-143">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="63154-144">Aby utworzyć kontekst miejsca do magazynowania, możesz użyć polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="63154-144">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="63154-145">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="63154-145">-ContinuationToken</span></span>
<span data-ttu-id="63154-146">Określa token kontynuacji listy obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="63154-146">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="63154-147">Ten parametr oraz parametr *MaxCount* umożliwiają wyświetlanie listy obiektów BLOB w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="63154-147">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63154-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63154-148">-DefaultProfile</span></span>
<span data-ttu-id="63154-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63154-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63154-150">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="63154-150">-IncludeDeleted</span></span>
<span data-ttu-id="63154-151">Dołączanie do usuniętego obiektu BLOB, domyślnie polecenie Pobierz obiekt BLOB nie uwzględnia usuniętego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="63154-151">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="63154-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="63154-152">-MaxCount</span></span>
<span data-ttu-id="63154-153">Określa maksymalną liczbę obiektów, które zostanie zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63154-153">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="63154-154">-Prefix</span><span class="sxs-lookup"><span data-stu-id="63154-154">-Prefix</span></span>
<span data-ttu-id="63154-155">Określa prefiks nazw obiektów blob, które należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="63154-155">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="63154-156">Ten parametr nie obsługuje wyszukiwania za pomocą wyrażeń regularnych ani symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="63154-156">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="63154-157">Oznacza to, że jeśli kontener zawiera tylko obiekty blob o nazwie "my", "MyBlob1" i "MyBlob2", a użytkownik określi "-prefix \*", polecenie cmdlet nie zwraca żadnych obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="63154-157">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="63154-158">Jednak w przypadku określenia "-prefix my" polecenie cmdlet zwraca ciąg "my", "MyBlob1" i "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="63154-158">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="63154-159">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63154-159">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="63154-160">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="63154-160">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="63154-161">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="63154-161">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="63154-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63154-162">CommonParameters</span></span>
<span data-ttu-id="63154-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63154-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63154-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63154-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63154-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63154-165">INPUTS</span></span>

### <span data-ttu-id="63154-166">System. String</span><span class="sxs-lookup"><span data-stu-id="63154-166">System.String</span></span>

### <span data-ttu-id="63154-167">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="63154-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="63154-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63154-168">OUTPUTS</span></span>

### <span data-ttu-id="63154-169">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="63154-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="63154-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63154-170">NOTES</span></span>

## <span data-ttu-id="63154-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63154-171">RELATED LINKS</span></span>

[<span data-ttu-id="63154-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="63154-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="63154-173">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="63154-173">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="63154-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="63154-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


