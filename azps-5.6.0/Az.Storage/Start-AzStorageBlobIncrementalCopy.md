---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 772e97611d81362ffb3becea8875826110e822a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002225"
---
# <span data-ttu-id="0c09c-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="0c09c-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="0c09c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c09c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c09c-103">Uruchamianie operacji kopiowania przyrostowego z migawki obiektu blob strony do określonego docelowego obiektu blob strony.</span><span class="sxs-lookup"><span data-stu-id="0c09c-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="0c09c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c09c-104">SYNTAX</span></span>

### <span data-ttu-id="0c09c-105">ContainerInstance (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0c09c-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c09c-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="0c09c-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c09c-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="0c09c-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c09c-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="0c09c-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c09c-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="0c09c-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c09c-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c09c-110">DESCRIPTION</span></span>
<span data-ttu-id="0c09c-111">Uruchamianie operacji kopiowania przyrostowego z migawki obiektu blob strony do określonego docelowego obiektu blob strony.</span><span class="sxs-lookup"><span data-stu-id="0c09c-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="0c09c-112">Zobacz więcej szczegółów dotyczących tej funkcji w https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob programie .</span><span class="sxs-lookup"><span data-stu-id="0c09c-112">See more details of the feature in https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="0c09c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c09c-113">EXAMPLES</span></span>

### <span data-ttu-id="0c09c-114">Przykład 1. Rozpoczynanie operacji kopiowania przyrostowego według nazwy obiektu blob i czasu migawki</span><span class="sxs-lookup"><span data-stu-id="0c09c-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="0c09c-115">To polecenie uruchamia operację kopiowania przyrostowego według nazwy obiektu blob i czasu migawki</span><span class="sxs-lookup"><span data-stu-id="0c09c-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="0c09c-116">Przykład 2. Rozpoczynanie operacji kopiowania przyrostowego przy użyciu źródłowego uri</span><span class="sxs-lookup"><span data-stu-id="0c09c-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="0c09c-117">To polecenie uruchamia operację kopiowania przyrostowego przy użyciu źródłowego uri</span><span class="sxs-lookup"><span data-stu-id="0c09c-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="0c09c-118">Przykład 3. Rozpoczynanie operacji kopiowania przyrostowego przy użyciu potoku kontenera z usługi GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0c09c-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="0c09c-119">To polecenie uruchamia operację kopiowania przyrostowego przy użyciu potoku kontenera z usługi GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0c09c-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="0c09c-120">Przykład 4. Uruchomienie operacji kopiowania przyrostowego z obiektu CloudPageBlob do docelowego obiektu blob z nazwą obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0c09c-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="0c09c-121">To polecenie uruchamia operację kopiowania przyrostowego z obiektu CloudPageBlob do docelowego obiektu blob z nazwą obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0c09c-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="0c09c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c09c-122">PARAMETERS</span></span>

### <span data-ttu-id="0c09c-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="0c09c-123">-AbsoluteUri</span></span>
<span data-ttu-id="0c09c-124">Bezwzględne Uri do źródła.</span><span class="sxs-lookup"><span data-stu-id="0c09c-124">Absolute Uri to the source.</span></span> <span data-ttu-id="0c09c-125">Należy zauważyć, że poświadczenia powinny być podane w uri, jeśli źródło ich wymaga.</span><span class="sxs-lookup"><span data-stu-id="0c09c-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="0c09c-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c09c-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c09c-127">Maksymalny czas wykonywania po stronie klienta dla każdego żądania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="0c09c-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="0c09c-128">— CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0c09c-128">-CloudBlob</span></span>
<span data-ttu-id="0c09c-129">Obiekt CloudBlob z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c09c-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="0c09c-130">Możesz go utworzyć lub użyć Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c09c-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c09c-131">- CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0c09c-131">-CloudBlobContainer</span></span>
<span data-ttu-id="0c09c-132">Obiekt CloudBlobContainer z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c09c-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="0c09c-133">Możesz go utworzyć lub użyć Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c09c-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c09c-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c09c-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c09c-135">Całkowita ilość jednoczesnych zadań synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0c09c-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="0c09c-136">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="0c09c-136">The default value is 10.</span></span>

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

### <span data-ttu-id="0c09c-137">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0c09c-137">-Context</span></span>
<span data-ttu-id="0c09c-138">Źródłowy kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c09c-138">Source Azure Storage Context.</span></span> <span data-ttu-id="0c09c-139">Możesz go utworzyć, New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c09c-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0c09c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c09c-140">-DefaultProfile</span></span>
<span data-ttu-id="0c09c-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c09c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c09c-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="0c09c-142">-DestBlob</span></span>
<span data-ttu-id="0c09c-143">Nazwa obiektu blob miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="0c09c-143">Destination blob name</span></span>

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

### <span data-ttu-id="0c09c-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="0c09c-144">-DestCloudBlob</span></span>
<span data-ttu-id="0c09c-145">Docelowy obiekt CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0c09c-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c09c-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="0c09c-146">-DestContainer</span></span>
<span data-ttu-id="0c09c-147">Nazwa kontenera docelowego</span><span class="sxs-lookup"><span data-stu-id="0c09c-147">Destination container name</span></span>

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

### <span data-ttu-id="0c09c-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="0c09c-148">-DestContext</span></span>
<span data-ttu-id="0c09c-149">Kontekst docelowego magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c09c-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="0c09c-150">Możesz go utworzyć, New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c09c-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0c09c-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c09c-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c09c-152">Czas serwera dla każdego żądania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="0c09c-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="0c09c-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="0c09c-153">-SrcBlob</span></span>
<span data-ttu-id="0c09c-154">Nazwa obiektu blob strony źródłowej.</span><span class="sxs-lookup"><span data-stu-id="0c09c-154">Source page blob name.</span></span>

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

### <span data-ttu-id="0c09c-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0c09c-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="0c09c-156">Czas migawki obiektu blob strony źródłowej.</span><span class="sxs-lookup"><span data-stu-id="0c09c-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="0c09c-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="0c09c-157">-SrcContainer</span></span>
<span data-ttu-id="0c09c-158">Nazwa kontenera źródłowego</span><span class="sxs-lookup"><span data-stu-id="0c09c-158">Source Container name</span></span>

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

### <span data-ttu-id="0c09c-159">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c09c-159">-Confirm</span></span>
<span data-ttu-id="0c09c-160">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c09c-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c09c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c09c-161">-WhatIf</span></span>
<span data-ttu-id="0c09c-162">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c09c-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c09c-163">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c09c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c09c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c09c-164">CommonParameters</span></span>
<span data-ttu-id="0c09c-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c09c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c09c-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c09c-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c09c-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c09c-167">INPUTS</span></span>

### <span data-ttu-id="0c09c-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="0c09c-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="0c09c-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0c09c-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="0c09c-170">System.String</span><span class="sxs-lookup"><span data-stu-id="0c09c-170">System.String</span></span>

### <span data-ttu-id="0c09c-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0c09c-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c09c-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c09c-172">OUTPUTS</span></span>

### <span data-ttu-id="0c09c-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0c09c-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="0c09c-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c09c-174">NOTES</span></span>

## <span data-ttu-id="0c09c-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c09c-175">RELATED LINKS</span></span>
