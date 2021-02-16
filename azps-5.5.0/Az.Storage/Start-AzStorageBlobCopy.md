---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197491"
---
# <span data-ttu-id="6c3c0-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6c3c0-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="6c3c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3c0-103">Zaczyna kopiowanie obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="6c3c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c3c0-104">SYNTAX</span></span>

### <span data-ttu-id="6c3c0-105">ContainerName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="6c3c0-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="6c3c0-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="6c3c0-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6c3c0-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="6c3c0-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="6c3c0-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="6c3c0-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="6c3c0-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="6c3c0-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c3c0-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="6c3c0-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c3c0-115">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c3c0-115">DESCRIPTION</span></span>
<span data-ttu-id="6c3c0-116">Polecenie **cmdlet Start-AzStorageBlobCopy** zaczyna kopiować obiekt blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="6c3c0-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c3c0-117">EXAMPLES</span></span>

### <span data-ttu-id="6c3c0-118">Przykład 1. Kopiowanie nazwanego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="6c3c0-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="6c3c0-119">To polecenie uruchamia operację kopiowania obiektu blob o nazwie ContosoPlanning2015 z kontenera o nazwie ContosoUploads do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="6c3c0-120">Przykład 2. Uzyskiwanie kontenera w celu określenia obiektów blob do skopiowania</span><span class="sxs-lookup"><span data-stu-id="6c3c0-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="6c3c0-121">To polecenie pobiera kontener o nazwie ContosoUploads za pomocą polecenia cmdlet **Get-AzStorageContainer,** a następnie przekazuje kontener do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6c3c0-122">To polecenie cmdlet uruchamia operację kopiowania obiektu blob o nazwie ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="6c3c0-123">Poprzednie polecenie cmdlet udostępnia kontener źródłowy.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="6c3c0-124">Parametr *DestContainer* określa kontener docelowy ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="6c3c0-125">Przykład 3. Pobierz wszystkie obiekty blob w kontenerze i skopiuj je</span><span class="sxs-lookup"><span data-stu-id="6c3c0-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="6c3c0-126">To polecenie pobiera obiekty blob w kontenerze o nazwie ContosoUploads za pomocą polecenia cmdlet **Get-AzStorageBlob,** a następnie przekazuje wyniki do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6c3c0-127">To polecenie cmdlet uruchamia operację kopiowania obiektów blob do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="6c3c0-128">Przykład 4. Kopiowanie obiektu blob określonego jako obiekt</span><span class="sxs-lookup"><span data-stu-id="6c3c0-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="6c3c0-129">Pierwsze polecenie pobiera obiekt blob o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="6c3c0-130">Polecenie przechowuje ten obiekt w $SrcBlob zmienną.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="6c3c0-131">Drugie polecenie pobiera obiekt blob o nazwie ContosoPlanning2015Archived w kontenerze o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="6c3c0-132">Polecenie przechowuje ten obiekt w $DestBlob zmienną.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="6c3c0-133">Ostatnie polecenie uruchamia operację kopiowania z kontenera źródłowego do kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="6c3c0-134">To polecenie używa standardowej notacji kropki w celu określenia obiektów **ICloudBlob** dla obiektów blob $SrcBlob i $DestBlob blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="6c3c0-135">Przykład 5. Kopiowanie obiektu blob z URI</span><span class="sxs-lookup"><span data-stu-id="6c3c0-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="6c3c0-136">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, które używa określonego klucza, a następnie przechowuje ten klucz w $Context zmienną.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="6c3c0-137">Drugie polecenie kopiuje plik z określonego URI do obiektu blob o nazwie ContosoPlanning w kontenerze o nazwie ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="6c3c0-138">Polecenie uruchamia operację kopiowania do kontekstu docelowego przechowywanego w $Context.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="6c3c0-139">Nie ma kontekstu magazynu źródłowego, więc źródłowy identyfikator Uri musi mieć dostęp do obiektu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="6c3c0-140">Na przykład: jeśli źródłem jest żaden publiczny obiekt blob platformy Azure, ten obiekt Uri powinien zawierać token SAS, który ma dostęp do odczytu tego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="6c3c0-141">Przykład 6. Kopiowanie bloku obiektu blob do kontenera docelowego z nową nazwą obiektu blob i ustawianie docelowego obiektu blob StandardBlobTier jako typu Hot, RekatatePriority jako wysokiego</span><span class="sxs-lookup"><span data-stu-id="6c3c0-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="6c3c0-142">To polecenie uruchamia operację kopiowania bloku obiektu blob do kontenera docelowego z nową nazwą obiektu blob i ustaw docelowy obiekt blob StandardBlobTier jako hot, RejekatPriority jako Wysoki</span><span class="sxs-lookup"><span data-stu-id="6c3c0-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="6c3c0-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c3c0-143">PARAMETERS</span></span>

### <span data-ttu-id="6c3c0-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="6c3c0-144">-AbsoluteUri</span></span>
<span data-ttu-id="6c3c0-145">Określa bezwzględny URI pliku do skopiowania do obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="6c3c0-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6c3c0-146">-BlobBaseClient</span></span>
<span data-ttu-id="6c3c0-147">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6c3c0-147">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="6c3c0-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6c3c0-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6c3c0-149">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6c3c0-150">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6c3c0-151">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6c3c0-152">— CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6c3c0-152">-CloudBlob</span></span>
<span data-ttu-id="6c3c0-153">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6c3c0-154">Aby uzyskać obiekt **CloudBlob,** użyj Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6c3c0-155">- CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6c3c0-155">-CloudBlobContainer</span></span>
<span data-ttu-id="6c3c0-156">Określa obiekt **CloudBlobContainer** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6c3c0-157">To polecenie cmdlet kopiuje obiekt blob z kontenera, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="6c3c0-158">Aby uzyskać obiekt **CloudBlobContainer,** użyj Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6c3c0-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6c3c0-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6c3c0-160">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6c3c0-161">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6c3c0-162">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6c3c0-163">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6c3c0-164">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-164">The default value is 10.</span></span>

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

### <span data-ttu-id="6c3c0-165">— kontekst</span><span class="sxs-lookup"><span data-stu-id="6c3c0-165">-Context</span></span>
<span data-ttu-id="6c3c0-166">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6c3c0-167">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6c3c0-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c3c0-168">-DefaultProfile</span></span>
<span data-ttu-id="6c3c0-169">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c3c0-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="6c3c0-170">-DestBlob</span></span>
<span data-ttu-id="6c3c0-171">Określa nazwę docelowego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-171">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="6c3c0-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="6c3c0-172">-DestCloudBlob</span></span>
<span data-ttu-id="6c3c0-173">Określa obiekt **docelowy CloudBlob**</span><span class="sxs-lookup"><span data-stu-id="6c3c0-173">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="6c3c0-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="6c3c0-174">-DestContainer</span></span>
<span data-ttu-id="6c3c0-175">Określa nazwę kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-175">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="6c3c0-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="6c3c0-176">-DestContext</span></span>
<span data-ttu-id="6c3c0-177">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6c3c0-178">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6c3c0-179">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6c3c0-179">-Force</span></span>
<span data-ttu-id="6c3c0-180">Wskazuje, że to polecenie cmdlet zastępuje docelowy obiekt blob bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6c3c0-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="6c3c0-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="6c3c0-182">Warstwa obiektów blob strony premium</span><span class="sxs-lookup"><span data-stu-id="6c3c0-182">Premium Page Blob Tier</span></span>

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

### <span data-ttu-id="6c3c0-183">-RepatatePriority</span><span class="sxs-lookup"><span data-stu-id="6c3c0-183">-RehydratePriority</span></span>
<span data-ttu-id="6c3c0-184">Zablokuj ponowną dzierżawę obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="6c3c0-185">Wskazuje priorytet, z którym ma być ponownie wywrzeny zarchiwizowane obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="6c3c0-186">Prawidłowe wartości to Wysoka/Standardowa.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-186">Valid values are High/Standard.</span></span>

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

### <span data-ttu-id="6c3c0-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6c3c0-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6c3c0-188">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6c3c0-189">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6c3c0-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="6c3c0-190">-SrcBlob</span></span>
<span data-ttu-id="6c3c0-191">Określa nazwę źródłowego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-191">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="6c3c0-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="6c3c0-192">-SrcContainer</span></span>
<span data-ttu-id="6c3c0-193">Określa nazwę kontenera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="6c3c0-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="6c3c0-194">-SrcDir</span></span>
<span data-ttu-id="6c3c0-195">Określa obiekt **CloudFileDirectory** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="6c3c0-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="6c3c0-196">-SrcFile</span></span>
<span data-ttu-id="6c3c0-197">Określa obiekt **CloudFile** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6c3c0-198">Możesz go utworzyć lub użyć Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="6c3c0-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="6c3c0-199">-SrcFilePath</span></span>
<span data-ttu-id="6c3c0-200">Określa ścieżkę względną do pliku źródłowego katalogu źródłowego lub udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-200">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="6c3c0-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="6c3c0-201">-SrcShare</span></span>
<span data-ttu-id="6c3c0-202">Określa obiekt **CloudFileShare** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6c3c0-203">Możesz go utworzyć lub użyć Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="6c3c0-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="6c3c0-204">-SrcShareName</span></span>
<span data-ttu-id="6c3c0-205">Określa nazwę udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-205">Specifies the source share name.</span></span>

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

### <span data-ttu-id="6c3c0-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6c3c0-206">-StandardBlobTier</span></span>
<span data-ttu-id="6c3c0-207">Blokuj warstwę obiektów blob, prawidłowe wartości to hot/cool/archive.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="6c3c0-208">Zobacz szczegóły w https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="6c3c0-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="6c3c0-209">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c3c0-209">-Confirm</span></span>
<span data-ttu-id="6c3c0-210">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c3c0-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c3c0-211">-WhatIf</span></span>
<span data-ttu-id="6c3c0-212">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c3c0-213">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c3c0-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3c0-214">CommonParameters</span></span>
<span data-ttu-id="6c3c0-215">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c3c0-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3c0-216">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c3c0-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3c0-217">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c3c0-217">INPUTS</span></span>

### <span data-ttu-id="6c3c0-218">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6c3c0-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6c3c0-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6c3c0-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6c3c0-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="6c3c0-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="6c3c0-221">System.String</span><span class="sxs-lookup"><span data-stu-id="6c3c0-221">System.String</span></span>

### <span data-ttu-id="6c3c0-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c3c0-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6c3c0-223">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c3c0-223">OUTPUTS</span></span>

### <span data-ttu-id="6c3c0-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6c3c0-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6c3c0-225">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c3c0-225">NOTES</span></span>

## <span data-ttu-id="6c3c0-226">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c3c0-226">RELATED LINKS</span></span>

[<span data-ttu-id="6c3c0-227">Get-AzstorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="6c3c0-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="6c3c0-228">Stop-AzstorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6c3c0-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
