---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
ms.openlocfilehash: 5023643ae57ab73ea625254f7b2362c947209f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527166"
---
# <span data-ttu-id="a26b5-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a26b5-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="a26b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a26b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a26b5-103">Pobiera obiekt blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="a26b5-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a26b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a26b5-104">SYNTAX</span></span>

### <span data-ttu-id="a26b5-105">ReceiveManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a26b5-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a26b5-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a26b5-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a26b5-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a26b5-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a26b5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a26b5-108">DESCRIPTION</span></span>
<span data-ttu-id="a26b5-109">Polecenie cmdlet **Get-AzureStorageBlobContent** umożliwia pobranie określonego obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="a26b5-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="a26b5-110">Jeśli nazwa obiektu BLOB nie jest prawidłowa na komputerze lokalnym, to polecenie cmdlet automatycznie rozpoznaje je, jeśli to możliwe.</span><span class="sxs-lookup"><span data-stu-id="a26b5-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="a26b5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a26b5-111">EXAMPLES</span></span>

### <span data-ttu-id="a26b5-112">Przykład 1: pobieranie zawartości obiektu BLOB według nazwy</span><span class="sxs-lookup"><span data-stu-id="a26b5-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="a26b5-113">To polecenie umożliwia pobranie obiektu BLOB według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a26b5-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="a26b5-114">Przykład 2: pobieranie zawartości obiektu BLOB za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="a26b5-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="a26b5-115">To polecenie używa potoku do znajdowania i pobierania zawartości obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="a26b5-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="a26b5-116">Przykład 3: pobieranie zawartości obiektu BLOB za pomocą potoku i znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="a26b5-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="a26b5-117">W tym przykładzie użyto symbolu wieloznacznego gwiazdki i rurociągu do znajdowania i pobierania zawartości obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="a26b5-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="a26b5-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a26b5-118">PARAMETERS</span></span>

### <span data-ttu-id="a26b5-119">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="a26b5-119">-Blob</span></span>
<span data-ttu-id="a26b5-120">Określa nazwę obiektu BLOB, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="a26b5-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="a26b5-121">-CheckMd5</span></span>
<span data-ttu-id="a26b5-122">Określa, czy ma być sprawdzana suma Md5 dla pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="a26b5-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="a26b5-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a26b5-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a26b5-124">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="a26b5-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a26b5-125">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="a26b5-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a26b5-126">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="a26b5-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a26b5-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a26b5-127">-CloudBlob</span></span>
<span data-ttu-id="a26b5-128">Określa obiekt BLOB chmury.</span><span class="sxs-lookup"><span data-stu-id="a26b5-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="a26b5-129">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="a26b5-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a26b5-130">-CloudBlobContainer</span></span>
<span data-ttu-id="a26b5-131">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a26b5-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="a26b5-132">Możesz je utworzyć lub użyć Get-AzureStorageContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a26b5-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a26b5-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a26b5-134">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a26b5-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a26b5-135">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a26b5-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a26b5-136">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="a26b5-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a26b5-137">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="a26b5-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a26b5-138">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a26b5-138">The default value is 10.</span></span>

<span data-ttu-id="a26b5-139">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a26b5-139">The default value is 10.</span></span>

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

### <span data-ttu-id="a26b5-140">-Kontener</span><span class="sxs-lookup"><span data-stu-id="a26b5-140">-Container</span></span>
<span data-ttu-id="a26b5-141">Określa nazwę kontenera zawierającego obiekt BLOB, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="a26b5-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-142">-Context</span><span class="sxs-lookup"><span data-stu-id="a26b5-142">-Context</span></span>
<span data-ttu-id="a26b5-143">Określa konto usługi Azure Storage, z którego chcesz pobrać zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="a26b5-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="a26b5-144">Aby utworzyć kontekst miejsca do magazynowania, możesz użyć polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a26b5-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="a26b5-145">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="a26b5-145">-Destination</span></span>
<span data-ttu-id="a26b5-146">Określa lokalizację, w której ma zostać zapisany pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="a26b5-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-147">-Force</span><span class="sxs-lookup"><span data-stu-id="a26b5-147">-Force</span></span>
<span data-ttu-id="a26b5-148">Zastępuje istniejący plik bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a26b5-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="a26b5-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a26b5-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a26b5-150">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="a26b5-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a26b5-151">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="a26b5-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a26b5-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a26b5-152">-Confirm</span></span>
<span data-ttu-id="a26b5-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a26b5-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a26b5-154">-WhatIf</span></span>
<span data-ttu-id="a26b5-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a26b5-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a26b5-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a26b5-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26b5-157">CommonParameters</span></span>
<span data-ttu-id="a26b5-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a26b5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26b5-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a26b5-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26b5-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a26b5-160">INPUTS</span></span>

### <span data-ttu-id="a26b5-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a26b5-161">IStorageContext</span></span>

<span data-ttu-id="a26b5-162">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="a26b5-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="a26b5-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a26b5-163">OUTPUTS</span></span>

### <span data-ttu-id="a26b5-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a26b5-164">AzureStorageContainer</span></span>

## <span data-ttu-id="a26b5-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a26b5-165">NOTES</span></span>
* <span data-ttu-id="a26b5-166">Jeśli nazwa obiektu BLOB jest nieprawidłowa dla komputera lokalnego, to polecenie cmdlet automatycznie rozpoznaje je, jeśli jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="a26b5-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="a26b5-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a26b5-167">RELATED LINKS</span></span>

[<span data-ttu-id="a26b5-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a26b5-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="a26b5-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a26b5-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="a26b5-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a26b5-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
