---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b3e85a3cd5e892b34368e553821e888c230dfa94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548452"
---
# <span data-ttu-id="374a9-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="374a9-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="374a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="374a9-102">SYNOPSIS</span></span>
<span data-ttu-id="374a9-103">Zatrzymuje operację kopiowania.</span><span class="sxs-lookup"><span data-stu-id="374a9-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="374a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="374a9-104">SYNTAX</span></span>

### <span data-ttu-id="374a9-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="374a9-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="374a9-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="374a9-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="374a9-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="374a9-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="374a9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="374a9-108">DESCRIPTION</span></span>
<span data-ttu-id="374a9-109">Polecenie cmdlet **stop-AzureStorageBlobCopy** zatrzymuje operację kopiowania do określonego docelowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="374a9-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="374a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="374a9-110">EXAMPLES</span></span>

### <span data-ttu-id="374a9-111">Przykład 1: zatrzymywanie operacji kopiowania według nazwy</span><span class="sxs-lookup"><span data-stu-id="374a9-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="374a9-112">To polecenie zatrzymuje operację kopiowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="374a9-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="374a9-113">Przykład 2: zatrzymywanie operacji kopiowania za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="374a9-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="374a9-114">To polecenie zatrzymuje operację kopiowania, przesyłając kontener w rurociągu, korzystając z polecenia **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="374a9-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="374a9-115">Przykład 3: zatrzymywanie operacji kopiowania za pomocą potoku i Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="374a9-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="374a9-116">W tym przykładzie zatrzymano operację kopiowania, przesyłając kontener w potoku za pomocą polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="374a9-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="374a9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="374a9-117">PARAMETERS</span></span>

### <span data-ttu-id="374a9-118">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="374a9-118">-Blob</span></span>
<span data-ttu-id="374a9-119">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="374a9-119">Specifies the name of the blob.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a9-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="374a9-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="374a9-121">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="374a9-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="374a9-122">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="374a9-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="374a9-123">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="374a9-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="374a9-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="374a9-124">-CloudBlob</span></span>
<span data-ttu-id="374a9-125">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="374a9-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="374a9-126">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="374a9-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="374a9-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="374a9-127">-CloudBlobContainer</span></span>
<span data-ttu-id="374a9-128">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="374a9-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="374a9-129">Możesz utworzyć obiekt lub użyć Get-AzureStorageContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="374a9-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="374a9-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="374a9-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="374a9-131">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="374a9-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="374a9-132">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="374a9-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="374a9-133">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="374a9-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="374a9-134">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="374a9-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="374a9-135">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="374a9-135">The default value is 10.</span></span>

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

### <span data-ttu-id="374a9-136">-Kontener</span><span class="sxs-lookup"><span data-stu-id="374a9-136">-Container</span></span>
<span data-ttu-id="374a9-137">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="374a9-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a9-138">-Context</span><span class="sxs-lookup"><span data-stu-id="374a9-138">-Context</span></span>
<span data-ttu-id="374a9-139">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="374a9-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="374a9-140">Kontekst można utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="374a9-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="374a9-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="374a9-141">-CopyId</span></span>
<span data-ttu-id="374a9-142">Określa identyfikator kopii.</span><span class="sxs-lookup"><span data-stu-id="374a9-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a9-143">-Force</span><span class="sxs-lookup"><span data-stu-id="374a9-143">-Force</span></span>
<span data-ttu-id="374a9-144">Zatrzymuje bieżące zadanie kopiowania na określonym obiekcie blob bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="374a9-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="374a9-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="374a9-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="374a9-146">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="374a9-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="374a9-147">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="374a9-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="374a9-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="374a9-148">-Confirm</span></span>
<span data-ttu-id="374a9-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="374a9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="374a9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="374a9-150">-WhatIf</span></span>
<span data-ttu-id="374a9-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="374a9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="374a9-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="374a9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="374a9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374a9-153">CommonParameters</span></span>
<span data-ttu-id="374a9-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="374a9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374a9-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="374a9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374a9-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="374a9-156">INPUTS</span></span>

### <span data-ttu-id="374a9-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="374a9-157">IStorageContext</span></span>

<span data-ttu-id="374a9-158">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="374a9-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="374a9-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="374a9-159">OUTPUTS</span></span>

### <span data-ttu-id="374a9-160">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="374a9-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="374a9-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="374a9-161">NOTES</span></span>

## <span data-ttu-id="374a9-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="374a9-162">RELATED LINKS</span></span>

[<span data-ttu-id="374a9-163">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="374a9-163">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="374a9-164">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="374a9-164">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="374a9-165">Start — AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="374a9-165">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="374a9-166">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="374a9-166">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
