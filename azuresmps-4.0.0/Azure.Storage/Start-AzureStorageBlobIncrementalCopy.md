---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc15650b9a3cf16b1448b5e971669fbd37733b94
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522565"
---
# <span data-ttu-id="1dead-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="1dead-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="1dead-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dead-102">SYNOPSIS</span></span>
<span data-ttu-id="1dead-103">Rozpocznij operację przyrostowa kopiowania z migawki obiektu BLOB strony do określonego obiektu BLOB strony docelowej.</span><span class="sxs-lookup"><span data-stu-id="1dead-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="1dead-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dead-104">SYNTAX</span></span>

### <span data-ttu-id="1dead-105">ContainerInstance (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1dead-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1dead-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="1dead-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1dead-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="1dead-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1dead-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="1dead-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1dead-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="1dead-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1dead-110">Opis</span><span class="sxs-lookup"><span data-stu-id="1dead-110">DESCRIPTION</span></span>
<span data-ttu-id="1dead-111">Rozpocznij operację przyrostowa kopiowania z migawki obiektu BLOB strony do określonego obiektu BLOB strony docelowej.</span><span class="sxs-lookup"><span data-stu-id="1dead-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="1dead-112">Zobacz więcej szczegółów dotyczących funkcji https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="1dead-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="1dead-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dead-113">EXAMPLES</span></span>

### <span data-ttu-id="1dead-114">Przykład 1. Rozpocznij operację przyrostowej kopii według nazwy obiektu BLOB i czasu migawki</span><span class="sxs-lookup"><span data-stu-id="1dead-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="1dead-115">To polecenie rozpoczyna przyrostowe operacje kopiowania według nazwy obiektu BLOB i czasu migawki</span><span class="sxs-lookup"><span data-stu-id="1dead-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="1dead-116">Przykład 2. Rozpocznij operację przyrostowej kopii przy użyciu źródłowego identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="1dead-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="1dead-117">To polecenie rozpoczyna przyrostową operację kopiowania przy użyciu źródłowego identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="1dead-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="1dead-118">Przykład 3: Rozpoczynanie przyrostowej operacji kopiowania przy użyciu rurociągu kontenera z GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1dead-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="1dead-119">To polecenie rozpoczyna przyrostową operację kopiowania przy użyciu potoku kontenera od GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1dead-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="1dead-120">Przykład 4: Rozpoczynanie przyrostowej operacji kopiowania z obiektu CloudPageBlob do docelowego obiektu BLOB przy użyciu nazwy obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="1dead-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="1dead-121">To polecenie rozpoczyna przyrostową operację kopiowania z obiektu CloudPageBlob do docelowego obiektu BLOB z nazwą obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="1dead-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="1dead-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dead-122">PARAMETERS</span></span>

### <span data-ttu-id="1dead-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="1dead-123">-AbsoluteUri</span></span>
<span data-ttu-id="1dead-124">Bezwzględny identyfikator URI do źródła.</span><span class="sxs-lookup"><span data-stu-id="1dead-124">Absolute Uri to the source.</span></span>
<span data-ttu-id="1dead-125">Należy zauważyć, że poświadczenia powinny być podane w identyfikatorze URI, jeśli źródło wymaga dowolnych danych.</span><span class="sxs-lookup"><span data-stu-id="1dead-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1dead-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1dead-127">Maksymalny czas wykonywania wszystkich żądań po stronie klienta (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="1dead-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="1dead-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1dead-128">-CloudBlob</span></span>
<span data-ttu-id="1dead-129">Obiekt CloudBlob z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1dead-129">CloudBlob object from Azure Storage Client library.</span></span>
<span data-ttu-id="1dead-130">Możesz je utworzyć lub użyć Get-AzureStorageBlob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dead-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1dead-131">-CloudBlobContainer</span></span>
<span data-ttu-id="1dead-132">Obiekt CloudBlobContainer z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1dead-132">CloudBlobContainer object from Azure Storage Client library.</span></span>
<span data-ttu-id="1dead-133">Możesz je utworzyć lub użyć Get-AzureStorageContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dead-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1dead-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1dead-135">Całkowita liczba współbieżnych zadań asynchronicznych.</span><span class="sxs-lookup"><span data-stu-id="1dead-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="1dead-136">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="1dead-136">The default value is 10.</span></span>

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

### <span data-ttu-id="1dead-137">-Context</span><span class="sxs-lookup"><span data-stu-id="1dead-137">-Context</span></span>
<span data-ttu-id="1dead-138">Kontekst źródłowy usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1dead-138">Source Azure Storage Context.</span></span>
<span data-ttu-id="1dead-139">Możesz je utworzyć, New-AzureStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dead-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="1dead-140">-DestBlob</span></span>
<span data-ttu-id="1dead-141">Nazwa docelowego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="1dead-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="1dead-142">-DestCloudBlob</span></span>
<span data-ttu-id="1dead-143">Obiekt docelowy CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1dead-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="1dead-144">-DestContainer</span></span>
<span data-ttu-id="1dead-145">Nazwa kontenera docelowego</span><span class="sxs-lookup"><span data-stu-id="1dead-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-146">-DestContext</span><span class="sxs-lookup"><span data-stu-id="1dead-146">-DestContext</span></span>
<span data-ttu-id="1dead-147">Kontekst miejsca docelowego usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1dead-147">Destination Azure Storage Context.</span></span>
<span data-ttu-id="1dead-148">Możesz je utworzyć, New-AzureStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dead-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1dead-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1dead-150">Upłynął limit czasu serwera dla każdego żądania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="1dead-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="1dead-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="1dead-151">-SrcBlob</span></span>
<span data-ttu-id="1dead-152">Nazwa obiektu BLOB strony źródłowej.</span><span class="sxs-lookup"><span data-stu-id="1dead-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="1dead-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="1dead-154">Czas migawki obiektu BLOB strony źródłowej.</span><span class="sxs-lookup"><span data-stu-id="1dead-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="1dead-155">-SrcContainer</span></span>
<span data-ttu-id="1dead-156">Nazwa kontenera źródłowego</span><span class="sxs-lookup"><span data-stu-id="1dead-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dead-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1dead-157">-Confirm</span></span>
<span data-ttu-id="1dead-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dead-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dead-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dead-159">-WhatIf</span></span>
<span data-ttu-id="1dead-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dead-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dead-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1dead-161">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="1dead-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dead-162">INPUTS</span></span>

### <span data-ttu-id="1dead-163">Microsoft. platformy windowsazure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="1dead-163">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="1dead-164">Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer system. String Microsoft. platformy windowsazure. Commands. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1dead-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="1dead-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dead-165">OUTPUTS</span></span>

### <span data-ttu-id="1dead-166">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1dead-166">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="1dead-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dead-167">NOTES</span></span>

## <span data-ttu-id="1dead-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dead-168">RELATED LINKS</span></span>

