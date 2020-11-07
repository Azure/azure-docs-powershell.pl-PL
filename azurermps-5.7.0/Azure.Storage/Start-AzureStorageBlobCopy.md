---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobCopy.md
ms.openlocfilehash: 054aa003752c27849c44eb00654313c395c255ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718068"
---
# <span data-ttu-id="5e974-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5e974-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="5e974-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e974-102">SYNOPSIS</span></span>
<span data-ttu-id="5e974-103">Rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="5e974-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e974-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e974-104">SYNTAX</span></span>

### <span data-ttu-id="5e974-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5e974-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="5e974-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="5e974-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5e974-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-109">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="5e974-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="5e974-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="5e974-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="5e974-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="5e974-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e974-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="5e974-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e974-115">Opis</span><span class="sxs-lookup"><span data-stu-id="5e974-115">DESCRIPTION</span></span>
<span data-ttu-id="5e974-116">Polecenie cmdlet **Start-AzureStorageBlobCopy** rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="5e974-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="5e974-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e974-117">EXAMPLES</span></span>

### <span data-ttu-id="5e974-118">Przykład 1: kopiowanie nazwanego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="5e974-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="5e974-119">To polecenie uruchamia operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015 z kontenera o nazwie ContosoUploads do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="5e974-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="5e974-120">Przykład 2: Uzyskaj kontener określający obiekty blob do skopiowania</span><span class="sxs-lookup"><span data-stu-id="5e974-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="5e974-121">To polecenie uzyskuje kontener o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzureStorageContainer** , a następnie przekazuje kontener do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5e974-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5e974-122">To polecenie cmdlet rozpoczyna operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="5e974-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="5e974-123">Poprzednie polecenie cmdlet udostępnia kontener źródłowy.</span><span class="sxs-lookup"><span data-stu-id="5e974-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="5e974-124">Parametr *DestContainer* określa ContosoArchives jako kontener docelowy.</span><span class="sxs-lookup"><span data-stu-id="5e974-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="5e974-125">Przykład 3: pobieranie wszystkich obiektów BLOB w kontenerze i ich kopiowanie</span><span class="sxs-lookup"><span data-stu-id="5e974-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="5e974-126">To polecenie pobiera obiekty blob w kontenerze o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzureStorageBlob** , a następnie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5e974-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5e974-127">To polecenie cmdlet rozpoczyna operację kopiowania obiektów BLOB do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="5e974-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="5e974-128">Przykład 4: Kopiowanie obiektu blob określonego jako obiekt</span><span class="sxs-lookup"><span data-stu-id="5e974-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="5e974-129">Pierwsze polecenie uzyskuje obiekt BLOB o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="5e974-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="5e974-130">Polecenie zapisuje ten obiekt w zmiennej $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="5e974-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="5e974-131">Drugie polecenie pobiera obiekt BLOB o nazwie ContosoPlanning2015Archived w kontenerze o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="5e974-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="5e974-132">Polecenie zapisuje ten obiekt w zmiennej $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="5e974-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="5e974-133">Ostatnie polecenie rozpoczyna operację kopiowania z kontenera źródłowego do kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="5e974-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="5e974-134">W poleceniu użyto standardowego zapisu kropkowego do określenia obiektów **ICloudBlob** $SrcBlob i $DestBlob obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="5e974-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="5e974-135">Przykład 5: Kopiowanie obiektu BLOB z identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="5e974-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="5e974-136">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten klucz w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="5e974-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="5e974-137">Drugie polecenie skopiuje plik z określonego identyfikatora URI do obiektu BLOB o nazwie ContosoPlanning w kontenerze o nazwie ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="5e974-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="5e974-138">Polecenie rozpoczyna operację kopiowania w kontekście przechowywanym w $Context.</span><span class="sxs-lookup"><span data-stu-id="5e974-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="5e974-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e974-139">PARAMETERS</span></span>

### <span data-ttu-id="5e974-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="5e974-140">-AbsoluteUri</span></span>
<span data-ttu-id="5e974-141">Określa bezwzględny identyfikator URI pliku, który ma zostać skopiowany do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5e974-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="5e974-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5e974-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5e974-143">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="5e974-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5e974-144">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="5e974-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5e974-145">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="5e974-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5e974-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5e974-146">-CloudBlob</span></span>
<span data-ttu-id="5e974-147">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e974-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="5e974-148">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="5e974-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="5e974-149">-CloudBlobContainer</span></span>
<span data-ttu-id="5e974-150">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e974-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="5e974-151">To polecenie cmdlet umożliwia skopiowanie obiektu BLOB z kontenera, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="5e974-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="5e974-152">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="5e974-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="5e974-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5e974-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5e974-154">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5e974-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5e974-155">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5e974-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5e974-156">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="5e974-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5e974-157">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="5e974-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5e974-158">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="5e974-158">The default value is 10.</span></span>

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

### <span data-ttu-id="5e974-159">-Context</span><span class="sxs-lookup"><span data-stu-id="5e974-159">-Context</span></span>
<span data-ttu-id="5e974-160">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5e974-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5e974-161">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5e974-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="5e974-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="5e974-162">-DestBlob</span></span>
<span data-ttu-id="5e974-163">Określa nazwę docelowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="5e974-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="5e974-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="5e974-164">-DestCloudBlob</span></span>
<span data-ttu-id="5e974-165">Określa docelowy obiekt **CloudBlob**</span><span class="sxs-lookup"><span data-stu-id="5e974-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="5e974-166">-DestContainer</span></span>
<span data-ttu-id="5e974-167">Określa nazwę kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="5e974-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-168">-DestContext</span><span class="sxs-lookup"><span data-stu-id="5e974-168">-DestContext</span></span>
<span data-ttu-id="5e974-169">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5e974-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5e974-170">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5e974-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5e974-171">-Force</span><span class="sxs-lookup"><span data-stu-id="5e974-171">-Force</span></span>
<span data-ttu-id="5e974-172">Wskazuje, że to polecenie cmdlet zastępuje docelowy obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e974-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="5e974-173">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="5e974-173">-PremiumPageBlobTier</span></span>
<span data-ttu-id="5e974-174">Warstwa obiektu BLOB strony Premium</span><span class="sxs-lookup"><span data-stu-id="5e974-174">Premium Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5e974-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5e974-176">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="5e974-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="5e974-177">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="5e974-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="5e974-178">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="5e974-178">-SrcBlob</span></span>
<span data-ttu-id="5e974-179">Określa nazwę źródłowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="5e974-179">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-180">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="5e974-180">-SrcContainer</span></span>
<span data-ttu-id="5e974-181">Określa nazwę kontenera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="5e974-181">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="5e974-182">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="5e974-182">-SrcDir</span></span>
<span data-ttu-id="5e974-183">Określa obiekt **CloudFileDirectory** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e974-183">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-184">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="5e974-184">-SrcFile</span></span>
<span data-ttu-id="5e974-185">Specifes obiekt **CloudFile** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e974-185">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="5e974-186">Możesz je utworzyć lub użyć Get-AzureStorageFile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e974-186">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-187">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="5e974-187">-SrcFilePath</span></span>
<span data-ttu-id="5e974-188">Określa względną ścieżkę pliku źródłowego katalogu źródłowego lub udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="5e974-188">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-189">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="5e974-189">-SrcShare</span></span>
<span data-ttu-id="5e974-190">Określa obiekt **CloudFileShare** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e974-190">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="5e974-191">Możesz je utworzyć lub użyć Get-AzureStorageShare polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e974-191">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-192">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="5e974-192">-SrcShareName</span></span>
<span data-ttu-id="5e974-193">Określa nazwę udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="5e974-193">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e974-194">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e974-194">-Confirm</span></span>
<span data-ttu-id="5e974-195">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e974-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e974-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e974-196">-WhatIf</span></span>
<span data-ttu-id="5e974-197">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e974-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e974-198">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e974-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e974-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e974-199">CommonParameters</span></span>
<span data-ttu-id="5e974-200">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e974-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e974-201">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e974-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e974-202">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e974-202">INPUTS</span></span>

### <span data-ttu-id="5e974-203">CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5e974-203">CloudBlob</span></span>

<span data-ttu-id="5e974-204">Parametr "CloudBlob" akceptuje wartość typu "CloudBlob" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5e974-204">Parameter 'CloudBlob' accepts value of type 'CloudBlob' from the pipeline</span></span>

### <span data-ttu-id="5e974-205">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5e974-205">IStorageContext</span></span>

<span data-ttu-id="5e974-206">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="5e974-206">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5e974-207">CloudFile</span><span class="sxs-lookup"><span data-stu-id="5e974-207">CloudFile</span></span>

<span data-ttu-id="5e974-208">Parametr "SrcFile" akceptuje wartość typu "CloudFile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5e974-208">Parameter 'SrcFile' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="5e974-209">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e974-209">OUTPUTS</span></span>

### <span data-ttu-id="5e974-210">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5e974-210">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="5e974-211">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e974-211">NOTES</span></span>

## <span data-ttu-id="5e974-212">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e974-212">RELATED LINKS</span></span>

[<span data-ttu-id="5e974-213">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="5e974-213">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="5e974-214">Zatrzymaj — AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5e974-214">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
