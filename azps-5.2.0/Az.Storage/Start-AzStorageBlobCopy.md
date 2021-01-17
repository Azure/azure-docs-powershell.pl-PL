---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338830"
---
# <span data-ttu-id="24577-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="24577-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="24577-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24577-102">SYNOPSIS</span></span>
<span data-ttu-id="24577-103">Rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="24577-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="24577-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24577-104">SYNTAX</span></span>

### <span data-ttu-id="24577-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="24577-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24577-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="24577-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24577-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="24577-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24577-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="24577-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24577-109">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="24577-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24577-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="24577-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24577-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="24577-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24577-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="24577-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24577-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="24577-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24577-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="24577-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24577-115">Opis</span><span class="sxs-lookup"><span data-stu-id="24577-115">DESCRIPTION</span></span>
<span data-ttu-id="24577-116">Polecenie cmdlet **Start-AzStorageBlobCopy** rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="24577-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="24577-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24577-117">EXAMPLES</span></span>

### <span data-ttu-id="24577-118">Przykład 1: kopiowanie nazwanego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="24577-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="24577-119">To polecenie uruchamia operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015 z kontenera o nazwie ContosoUploads do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="24577-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="24577-120">Przykład 2: Uzyskaj kontener określający obiekty blob do skopiowania</span><span class="sxs-lookup"><span data-stu-id="24577-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="24577-121">To polecenie uzyskuje kontener o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzStorageContainer** , a następnie przekazuje kontener do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="24577-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="24577-122">To polecenie cmdlet rozpoczyna operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="24577-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="24577-123">Poprzednie polecenie cmdlet udostępnia kontener źródłowy.</span><span class="sxs-lookup"><span data-stu-id="24577-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="24577-124">Parametr *DestContainer* określa ContosoArchives jako kontener docelowy.</span><span class="sxs-lookup"><span data-stu-id="24577-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="24577-125">Przykład 3: pobieranie wszystkich obiektów BLOB w kontenerze i ich kopiowanie</span><span class="sxs-lookup"><span data-stu-id="24577-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="24577-126">To polecenie pobiera obiekty blob w kontenerze o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzStorageBlob** , a następnie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="24577-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="24577-127">To polecenie cmdlet rozpoczyna operację kopiowania obiektów BLOB do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="24577-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="24577-128">Przykład 4: Kopiowanie obiektu blob określonego jako obiekt</span><span class="sxs-lookup"><span data-stu-id="24577-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="24577-129">Pierwsze polecenie uzyskuje obiekt BLOB o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="24577-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="24577-130">Polecenie zapisuje ten obiekt w zmiennej $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="24577-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="24577-131">Drugie polecenie pobiera obiekt BLOB o nazwie ContosoPlanning2015Archived w kontenerze o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="24577-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="24577-132">Polecenie zapisuje ten obiekt w zmiennej $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="24577-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="24577-133">Ostatnie polecenie rozpoczyna operację kopiowania z kontenera źródłowego do kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="24577-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="24577-134">W poleceniu użyto standardowego zapisu kropkowego do określenia obiektów **ICloudBlob** $SrcBlob i $DestBlob obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="24577-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="24577-135">Przykład 5: Kopiowanie obiektu BLOB z identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="24577-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="24577-136">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten klucz w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="24577-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="24577-137">Drugie polecenie skopiuje plik z określonego identyfikatora URI do obiektu BLOB o nazwie ContosoPlanning w kontenerze o nazwie ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="24577-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="24577-138">Polecenie rozpoczyna operację kopiowania w kontekście docelowym przechowywanym w $Context.</span><span class="sxs-lookup"><span data-stu-id="24577-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="24577-139">Brak kontekstu magazynu źródłowego, więc źródłowy identyfikator URI musi mieć dostęp do obiektu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="24577-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="24577-140">Na przykład: Jeśli źródło nie ma publicznego obiektu blob platformy Azure, identyfikator URI powinien zawierać token SAS, który ma dostęp do odczytu do obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="24577-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="24577-141">Przykład 6: Kopiowanie bloku obiektu BLOB do kontenera docelowego przy użyciu nowej nazwy obiektu BLOB i Ustawianie obiektu BLOB StandardBlobTier jako Hot, RehydratePriority jako High</span><span class="sxs-lookup"><span data-stu-id="24577-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="24577-142">To polecenie uruchamia operację kopiowania bloku docelowego w kontenerze docelowym przy użyciu nowej nazwy obiektu BLOB i ustawia wartość docelową obiektu BLOB StandardBlobTier jako gorąca, RehydratePriority jako wysoka</span><span class="sxs-lookup"><span data-stu-id="24577-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="24577-143">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24577-143">PARAMETERS</span></span>

### <span data-ttu-id="24577-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="24577-144">-AbsoluteUri</span></span>
<span data-ttu-id="24577-145">Określa bezwzględny identyfikator URI pliku, który ma zostać skopiowany do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="24577-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="24577-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="24577-146">-BlobBaseClient</span></span>
<span data-ttu-id="24577-147">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="24577-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24577-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="24577-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="24577-149">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="24577-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="24577-150">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="24577-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="24577-151">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="24577-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="24577-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="24577-152">-CloudBlob</span></span>
<span data-ttu-id="24577-153">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24577-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="24577-154">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="24577-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24577-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="24577-155">-CloudBlobContainer</span></span>
<span data-ttu-id="24577-156">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24577-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="24577-157">To polecenie cmdlet umożliwia skopiowanie obiektu BLOB z kontenera, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="24577-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="24577-158">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="24577-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="24577-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="24577-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="24577-160">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="24577-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="24577-161">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="24577-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="24577-162">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="24577-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="24577-163">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="24577-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="24577-164">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="24577-164">The default value is 10.</span></span>

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

### <span data-ttu-id="24577-165">-Context</span><span class="sxs-lookup"><span data-stu-id="24577-165">-Context</span></span>
<span data-ttu-id="24577-166">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="24577-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="24577-167">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="24577-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="24577-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24577-168">-DefaultProfile</span></span>
<span data-ttu-id="24577-169">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24577-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24577-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="24577-170">-DestBlob</span></span>
<span data-ttu-id="24577-171">Określa nazwę docelowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="24577-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="24577-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="24577-172">-DestCloudBlob</span></span>
<span data-ttu-id="24577-173">Określa docelowy obiekt **CloudBlob**</span><span class="sxs-lookup"><span data-stu-id="24577-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="24577-174">-DestContainer</span></span>
<span data-ttu-id="24577-175">Określa nazwę kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="24577-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="24577-176">-DestContext</span></span>
<span data-ttu-id="24577-177">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="24577-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="24577-178">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="24577-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="24577-179">-Force</span><span class="sxs-lookup"><span data-stu-id="24577-179">-Force</span></span>
<span data-ttu-id="24577-180">Wskazuje, że to polecenie cmdlet zastępuje docelowy obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24577-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="24577-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="24577-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="24577-182">Warstwa obiektu BLOB strony Premium</span><span class="sxs-lookup"><span data-stu-id="24577-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="24577-183">-RehydratePriority</span></span>
<span data-ttu-id="24577-184">Blokowanie obiektu BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="24577-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="24577-185">Wskazuje priorytet, za pomocą którego można rehydratacji zarchiwizowany obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="24577-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="24577-186">Prawidłowe wartości to High/Standard.</span><span class="sxs-lookup"><span data-stu-id="24577-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="24577-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="24577-188">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="24577-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="24577-189">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="24577-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="24577-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="24577-190">-SrcBlob</span></span>
<span data-ttu-id="24577-191">Określa nazwę źródłowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="24577-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="24577-192">-SrcContainer</span></span>
<span data-ttu-id="24577-193">Określa nazwę kontenera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="24577-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="24577-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="24577-194">-SrcDir</span></span>
<span data-ttu-id="24577-195">Określa obiekt **CloudFileDirectory** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24577-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="24577-196">-SrcFile</span></span>
<span data-ttu-id="24577-197">Określa obiekt **CloudFile** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24577-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="24577-198">Możesz je utworzyć lub użyć Get-AzStorageFile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24577-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24577-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="24577-199">-SrcFilePath</span></span>
<span data-ttu-id="24577-200">Określa względną ścieżkę pliku źródłowego katalogu źródłowego lub udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="24577-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="24577-201">-SrcShare</span></span>
<span data-ttu-id="24577-202">Określa obiekt **CloudFileShare** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24577-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="24577-203">Możesz je utworzyć lub użyć Get-AzStorageShare polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24577-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="24577-204">-SrcShareName</span></span>
<span data-ttu-id="24577-205">Określa nazwę udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="24577-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="24577-206">-StandardBlobTier</span></span>
<span data-ttu-id="24577-207">Blokada warstwy obiektu BLOB, prawidłowe wartości to Hot/chłodna/archiwum.</span><span class="sxs-lookup"><span data-stu-id="24577-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="24577-208">Zobacz szczegóły https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="24577-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-209">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24577-209">-Confirm</span></span>
<span data-ttu-id="24577-210">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24577-210">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24577-211">-WhatIf</span></span>
<span data-ttu-id="24577-212">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24577-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24577-213">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24577-213">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24577-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24577-214">CommonParameters</span></span>
<span data-ttu-id="24577-215">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24577-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24577-216">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24577-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24577-217">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24577-217">INPUTS</span></span>

### <span data-ttu-id="24577-218">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="24577-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="24577-219">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="24577-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="24577-220">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="24577-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="24577-221">System. String</span><span class="sxs-lookup"><span data-stu-id="24577-221">System.String</span></span>

### <span data-ttu-id="24577-222">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="24577-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="24577-223">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24577-223">OUTPUTS</span></span>

### <span data-ttu-id="24577-224">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="24577-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="24577-225">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24577-225">NOTES</span></span>

## <span data-ttu-id="24577-226">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24577-226">RELATED LINKS</span></span>

[<span data-ttu-id="24577-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="24577-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="24577-228">Zatrzymaj — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="24577-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
