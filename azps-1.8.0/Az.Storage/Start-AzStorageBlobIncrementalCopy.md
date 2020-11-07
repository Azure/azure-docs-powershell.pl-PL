---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: caaa36aa27cfb008fbbecced78f1fefc04958f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707488"
---
# <span data-ttu-id="ad57f-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="ad57f-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="ad57f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad57f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad57f-103">Rozpocznij operację przyrostowa kopiowania z migawki obiektu BLOB strony do określonego obiektu BLOB strony docelowej.</span><span class="sxs-lookup"><span data-stu-id="ad57f-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="ad57f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad57f-104">SYNTAX</span></span>

### <span data-ttu-id="ad57f-105">ContainerInstance (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ad57f-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad57f-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="ad57f-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad57f-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="ad57f-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad57f-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="ad57f-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad57f-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="ad57f-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad57f-110">Opis</span><span class="sxs-lookup"><span data-stu-id="ad57f-110">DESCRIPTION</span></span>
<span data-ttu-id="ad57f-111">Rozpocznij operację przyrostowa kopiowania z migawki obiektu BLOB strony do określonego obiektu BLOB strony docelowej.</span><span class="sxs-lookup"><span data-stu-id="ad57f-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="ad57f-112">Zobacz więcej szczegółów dotyczących funkcji https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="ad57f-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="ad57f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad57f-113">EXAMPLES</span></span>

### <span data-ttu-id="ad57f-114">Przykład 1. Rozpocznij operację przyrostowej kopii według nazwy obiektu BLOB i czasu migawki</span><span class="sxs-lookup"><span data-stu-id="ad57f-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="ad57f-115">To polecenie rozpoczyna przyrostowe operacje kopiowania według nazwy obiektu BLOB i czasu migawki</span><span class="sxs-lookup"><span data-stu-id="ad57f-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="ad57f-116">Przykład 2. Rozpocznij operację przyrostowej kopii przy użyciu źródłowego identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="ad57f-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="ad57f-117">To polecenie rozpoczyna przyrostową operację kopiowania przy użyciu źródłowego identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="ad57f-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="ad57f-118">Przykład 3: Rozpoczynanie przyrostowej operacji kopiowania przy użyciu rurociągu kontenera z GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad57f-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="ad57f-119">To polecenie rozpoczyna przyrostową operację kopiowania przy użyciu potoku kontenera od GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad57f-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="ad57f-120">Przykład 4: Rozpoczynanie przyrostowej operacji kopiowania z obiektu CloudPageBlob do docelowego obiektu BLOB przy użyciu nazwy obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="ad57f-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="ad57f-121">To polecenie rozpoczyna przyrostową operację kopiowania z obiektu CloudPageBlob do docelowego obiektu BLOB z nazwą obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="ad57f-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="ad57f-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad57f-122">PARAMETERS</span></span>

### <span data-ttu-id="ad57f-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="ad57f-123">-AbsoluteUri</span></span>
<span data-ttu-id="ad57f-124">Bezwzględny identyfikator URI do źródła.</span><span class="sxs-lookup"><span data-stu-id="ad57f-124">Absolute Uri to the source.</span></span> <span data-ttu-id="ad57f-125">Należy zauważyć, że poświadczenia powinny być podane w identyfikatorze URI, jeśli źródło wymaga dowolnych danych.</span><span class="sxs-lookup"><span data-stu-id="ad57f-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ad57f-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ad57f-127">Maksymalny czas wykonywania wszystkich żądań po stronie klienta (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="ad57f-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="ad57f-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ad57f-128">-CloudBlob</span></span>
<span data-ttu-id="ad57f-129">Obiekt CloudBlob z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad57f-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="ad57f-130">Możesz je utworzyć lub użyć Get-AzStorageBlob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad57f-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ad57f-131">-CloudBlobContainer</span></span>
<span data-ttu-id="ad57f-132">Obiekt CloudBlobContainer z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad57f-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="ad57f-133">Możesz je utworzyć lub użyć Get-AzStorageContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad57f-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ad57f-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ad57f-135">Całkowita liczba współbieżnych zadań asynchronicznych.</span><span class="sxs-lookup"><span data-stu-id="ad57f-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="ad57f-136">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="ad57f-136">The default value is 10.</span></span>

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

### <span data-ttu-id="ad57f-137">-Context</span><span class="sxs-lookup"><span data-stu-id="ad57f-137">-Context</span></span>
<span data-ttu-id="ad57f-138">Kontekst źródłowy usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ad57f-138">Source Azure Storage Context.</span></span> <span data-ttu-id="ad57f-139">Możesz je utworzyć, New-AzStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad57f-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad57f-140">-DefaultProfile</span></span>
<span data-ttu-id="ad57f-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad57f-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad57f-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="ad57f-142">-DestBlob</span></span>
<span data-ttu-id="ad57f-143">Nazwa docelowego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="ad57f-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="ad57f-144">-DestCloudBlob</span></span>
<span data-ttu-id="ad57f-145">Obiekt docelowy CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ad57f-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="ad57f-146">-DestContainer</span></span>
<span data-ttu-id="ad57f-147">Nazwa kontenera docelowego</span><span class="sxs-lookup"><span data-stu-id="ad57f-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="ad57f-148">-DestContext</span></span>
<span data-ttu-id="ad57f-149">Kontekst miejsca docelowego usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ad57f-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="ad57f-150">Możesz je utworzyć, New-AzStorageContext polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad57f-150">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ad57f-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ad57f-152">Upłynął limit czasu serwera dla każdego żądania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="ad57f-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="ad57f-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="ad57f-153">-SrcBlob</span></span>
<span data-ttu-id="ad57f-154">Nazwa obiektu BLOB strony źródłowej.</span><span class="sxs-lookup"><span data-stu-id="ad57f-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="ad57f-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="ad57f-156">Czas migawki obiektu BLOB strony źródłowej.</span><span class="sxs-lookup"><span data-stu-id="ad57f-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="ad57f-157">-SrcContainer</span></span>
<span data-ttu-id="ad57f-158">Nazwa kontenera źródłowego</span><span class="sxs-lookup"><span data-stu-id="ad57f-158">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad57f-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad57f-159">-Confirm</span></span>
<span data-ttu-id="ad57f-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad57f-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad57f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad57f-161">-WhatIf</span></span>
<span data-ttu-id="ad57f-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad57f-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad57f-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad57f-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad57f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad57f-164">CommonParameters</span></span>
<span data-ttu-id="ad57f-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad57f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad57f-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad57f-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad57f-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad57f-167">INPUTS</span></span>

### <span data-ttu-id="ad57f-168">Microsoft. platformy windowsazure. Storage. blob. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="ad57f-168">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="ad57f-169">Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ad57f-169">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ad57f-170">System. String</span><span class="sxs-lookup"><span data-stu-id="ad57f-170">System.String</span></span>

### <span data-ttu-id="ad57f-171">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad57f-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ad57f-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad57f-172">OUTPUTS</span></span>

### <span data-ttu-id="ad57f-173">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ad57f-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ad57f-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad57f-174">NOTES</span></span>

## <span data-ttu-id="ad57f-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad57f-175">RELATED LINKS</span></span>
