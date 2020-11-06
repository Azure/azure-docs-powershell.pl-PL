---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
ms.openlocfilehash: fba71dbac836fb6cc6551982945135e8e9410744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527165"
---
# <span data-ttu-id="8b464-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="8b464-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="8b464-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b464-102">SYNOPSIS</span></span>
<span data-ttu-id="8b464-103">Pobiera stan kopii obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b464-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b464-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b464-104">SYNTAX</span></span>

### <span data-ttu-id="8b464-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8b464-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8b464-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="8b464-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b464-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="8b464-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8b464-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8b464-108">DESCRIPTION</span></span>
<span data-ttu-id="8b464-109">Polecenie cmdlet **Get-AzureStorageBlobCopyState** Pobiera stan kopii obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8b464-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="8b464-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b464-110">EXAMPLES</span></span>

### <span data-ttu-id="8b464-111">Przykład 1. Pobieranie stanu kopii obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="8b464-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="8b464-112">To polecenie pobiera stan kopii obiektu BLOB o nazwie ContosoPlanning2015 w ContosoUploads kontenera.</span><span class="sxs-lookup"><span data-stu-id="8b464-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="8b464-113">Przykład 2: pobieranie stanu kopiowania obiektu BLOB za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="8b464-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="8b464-114">To polecenie pobiera obiekt BLOB o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads przy użyciu polecenia cmdlet **Get-AzureStorageBlob** , a następnie przekazuje wynik do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8b464-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b464-115">Polecenie cmdlet **Get-AzureStorageBlobCopyState** Pobiera stan kopii tego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="8b464-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="8b464-116">Przykład 3: pobieranie stanu kopiowania obiektu BLOB w kontenerze za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="8b464-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="8b464-117">To polecenie uzyskuje kontener o nazwie za pomocą polecenia cmdlet **Get-AzureStorageBlob** , a następnie przekazuje wynik do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b464-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="8b464-118">Polecenie cmdlet **Get-AzureStorageContainer** Pobiera stan kopii obiektu BLOB o nazwie ContosoPlanning2015 w tym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="8b464-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="8b464-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b464-119">PARAMETERS</span></span>

### <span data-ttu-id="8b464-120">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="8b464-120">-Blob</span></span>
<span data-ttu-id="8b464-121">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="8b464-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="8b464-122">To polecenie cmdlet pobiera stan operacji kopiowania obiektu BLOB dla obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8b464-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b464-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b464-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8b464-124">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="8b464-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8b464-125">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="8b464-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8b464-126">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="8b464-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b464-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8b464-127">-CloudBlob</span></span>
<span data-ttu-id="8b464-128">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b464-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8b464-129">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="8b464-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="8b464-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8b464-130">-CloudBlobContainer</span></span>
<span data-ttu-id="8b464-131">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b464-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="8b464-132">To polecenie cmdlet pobiera stan kopii obiektu BLOB w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8b464-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="8b464-133">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="8b464-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="8b464-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8b464-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8b464-135">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8b464-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8b464-136">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8b464-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8b464-137">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="8b464-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8b464-138">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="8b464-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8b464-139">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8b464-139">The default value is 10.</span></span>

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

### <span data-ttu-id="8b464-140">-Kontener</span><span class="sxs-lookup"><span data-stu-id="8b464-140">-Container</span></span>
<span data-ttu-id="8b464-141">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="8b464-141">Specifies the name of a container.</span></span>
<span data-ttu-id="8b464-142">To polecenie cmdlet pobiera stan kopii obiektu BLOB w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8b464-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b464-143">-Context</span><span class="sxs-lookup"><span data-stu-id="8b464-143">-Context</span></span>
<span data-ttu-id="8b464-144">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8b464-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8b464-145">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8b464-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8b464-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b464-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8b464-147">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="8b464-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8b464-148">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="8b464-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8b464-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8b464-149">-WaitForComplete</span></span>
<span data-ttu-id="8b464-150">Wskazuje, że to polecenie cmdlet oczekuje na zakończenie kopii.</span><span class="sxs-lookup"><span data-stu-id="8b464-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="8b464-151">Jeśli nie podano tego parametru, to polecenie cmdlet natychmiast zwraca wynik.</span><span class="sxs-lookup"><span data-stu-id="8b464-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="8b464-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b464-152">CommonParameters</span></span>
<span data-ttu-id="8b464-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b464-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b464-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b464-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b464-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b464-155">INPUTS</span></span>

### <span data-ttu-id="8b464-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b464-156">IStorageContext</span></span>

<span data-ttu-id="8b464-157">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="8b464-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8b464-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b464-158">OUTPUTS</span></span>

### <span data-ttu-id="8b464-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="8b464-159">CopyState</span></span>

## <span data-ttu-id="8b464-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b464-160">NOTES</span></span>

## <span data-ttu-id="8b464-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b464-161">RELATED LINKS</span></span>

[<span data-ttu-id="8b464-162">Start — AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8b464-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="8b464-163">Zatrzymaj — AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8b464-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


