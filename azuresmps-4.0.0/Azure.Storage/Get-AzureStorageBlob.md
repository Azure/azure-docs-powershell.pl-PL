---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
ms.openlocfilehash: f7b68be6981343d14f7d1d8530a0af3c3eee199c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524061"
---
# <span data-ttu-id="336b9-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="336b9-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="336b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="336b9-102">SYNOPSIS</span></span>
<span data-ttu-id="336b9-103">Zawiera listę obiektów BLOB w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="336b9-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="336b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="336b9-104">SYNTAX</span></span>

### <span data-ttu-id="336b9-105">Obiekt blobname (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="336b9-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="336b9-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="336b9-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="336b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="336b9-107">DESCRIPTION</span></span>
<span data-ttu-id="336b9-108">Polecenie cmdlet **Get-AzureStorageBlob** zawiera listę obiektów BLOB w określonym kontenerze na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="336b9-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="336b9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="336b9-109">EXAMPLES</span></span>

### <span data-ttu-id="336b9-110">Przykład 1: uzyskiwanie obiektu BLOB według nazwy obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="336b9-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="336b9-111">W tym poleceniu jest używana nazwa obiektu BLOB i symbol wieloznaczny w celu uzyskania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="336b9-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="336b9-112">Przykład 2: uzyskiwanie obiektu BLOB za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="336b9-112">Example 2: Get a blob by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

<span data-ttu-id="336b9-113">To polecenie używa potoku w celu uzyskania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="336b9-113">This command uses the pipeline to get a blob.</span></span>

### <span data-ttu-id="336b9-114">Przykład 3: uzyskiwanie obiektu BLOB według prefiksu nazwy</span><span class="sxs-lookup"><span data-stu-id="336b9-114">Example 3: Get a blob by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="336b9-115">To polecenie używa prefiksu nazwy w celu uzyskania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="336b9-115">This command uses a name prefix to get a blob.</span></span>

### <span data-ttu-id="336b9-116">Przykład 4: Wyświetlanie listy obiektów BLOB w wielu partiach</span><span class="sxs-lookup"><span data-stu-id="336b9-116">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="336b9-117">W tym przykładzie użyto parametrów *MaxCount* i *ContinuationToken* , aby wyświetlić obiekty blob magazynu platformy Azure w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="336b9-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="336b9-118">Pierwsze cztery polecenia umożliwiają przypisanie wartości do zmiennych w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="336b9-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="336b9-119">Piąte polecenie **określa instrukcję do wykonania,** która używa polecenia cmdlet **Get-AzureStorageBlob** w celu uzyskania dostępu do obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="336b9-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="336b9-120">Instrukcja zawiera token kontynuacji przechowywany w zmiennej $Token.</span><span class="sxs-lookup"><span data-stu-id="336b9-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="336b9-121">$Token zmienia się w trakcie uruchamiania pętli.</span><span class="sxs-lookup"><span data-stu-id="336b9-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="336b9-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="336b9-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="336b9-123">W poleceniu ostatnim użyto polecenia **echo** do wyświetlenia sumy.</span><span class="sxs-lookup"><span data-stu-id="336b9-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="336b9-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="336b9-124">PARAMETERS</span></span>

### <span data-ttu-id="336b9-125">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="336b9-125">-Blob</span></span>
<span data-ttu-id="336b9-126">Określa nazwę lub wzorzec nazwy, który może być wykorzystywany do wyszukiwania symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="336b9-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="336b9-127">Jeśli nie podano nazwy obiektu BLOB, polecenie cmdlet wyświetla wszystkie obiekty blob w określonym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="336b9-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="336b9-128">Jeśli wartość jest określona dla tego parametru, polecenie cmdlet wyświetla wszystkie obiekty blob z nazwami zgodnymi z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="336b9-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336b9-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="336b9-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="336b9-130">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="336b9-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="336b9-131">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="336b9-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="336b9-132">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="336b9-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="336b9-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="336b9-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="336b9-134">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="336b9-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="336b9-135">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="336b9-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="336b9-136">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="336b9-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="336b9-137">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="336b9-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="336b9-138">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="336b9-138">The default value is 10.</span></span>

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

### <span data-ttu-id="336b9-139">-Kontener</span><span class="sxs-lookup"><span data-stu-id="336b9-139">-Container</span></span>
<span data-ttu-id="336b9-140">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="336b9-140">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="336b9-141">-Context</span><span class="sxs-lookup"><span data-stu-id="336b9-141">-Context</span></span>
<span data-ttu-id="336b9-142">Określa konto usługi Azure Storage, z którego chcesz uzyskać listę obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="336b9-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="336b9-143">Aby utworzyć kontekst miejsca do magazynowania, możesz użyć polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="336b9-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="336b9-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="336b9-144">-ContinuationToken</span></span>
<span data-ttu-id="336b9-145">Określa token kontynuacji listy obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="336b9-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="336b9-146">Ten parametr oraz parametr *MaxCount* umożliwiają wyświetlanie listy obiektów BLOB w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="336b9-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

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

### <span data-ttu-id="336b9-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="336b9-147">-MaxCount</span></span>
<span data-ttu-id="336b9-148">Określa maksymalną liczbę obiektów, które zostanie zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="336b9-148">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="336b9-149">-Prefix</span><span class="sxs-lookup"><span data-stu-id="336b9-149">-Prefix</span></span>
<span data-ttu-id="336b9-150">Określa prefiks nazw obiektów blob, które należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="336b9-150">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="336b9-151">Ten parametr nie obsługuje wyszukiwania za pomocą wyrażeń regularnych ani symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="336b9-151">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="336b9-152">Oznacza to, że jeśli kontener zawiera tylko obiekty blob o nazwie "my", "MyBlob1" i "MyBlob2", a użytkownik określi "-prefix \*", polecenie cmdlet nie zwraca żadnych obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="336b9-152">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="336b9-153">Jednak w przypadku określenia "-prefix my" polecenie cmdlet zwraca ciąg "my", "MyBlob1" i "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="336b9-153">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="336b9-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="336b9-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="336b9-155">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="336b9-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="336b9-156">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="336b9-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="336b9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336b9-157">CommonParameters</span></span>
<span data-ttu-id="336b9-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="336b9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336b9-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="336b9-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336b9-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="336b9-160">INPUTS</span></span>

## <span data-ttu-id="336b9-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="336b9-161">OUTPUTS</span></span>

### <span data-ttu-id="336b9-162">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="336b9-162">AzureStorageBlob</span></span>

## <span data-ttu-id="336b9-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="336b9-163">NOTES</span></span>
* <span data-ttu-id="336b9-164">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="336b9-164">SYNOPSIS</span></span>

## <span data-ttu-id="336b9-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="336b9-165">RELATED LINKS</span></span>

[<span data-ttu-id="336b9-166">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="336b9-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="336b9-167">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="336b9-167">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="336b9-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="336b9-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


