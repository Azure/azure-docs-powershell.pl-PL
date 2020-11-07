---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: a990b168fcaf32deffd495b5eeb0f9a813f2f093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886729"
---
# <span data-ttu-id="90f26-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="90f26-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="90f26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90f26-102">SYNOPSIS</span></span>
<span data-ttu-id="90f26-103">Rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="90f26-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="90f26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90f26-104">SYNTAX</span></span>

### <span data-ttu-id="90f26-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="90f26-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90f26-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="90f26-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90f26-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="90f26-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90f26-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="90f26-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90f26-109">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="90f26-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f26-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="90f26-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f26-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="90f26-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f26-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="90f26-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f26-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="90f26-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90f26-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="90f26-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f26-115">Opis</span><span class="sxs-lookup"><span data-stu-id="90f26-115">DESCRIPTION</span></span>
<span data-ttu-id="90f26-116">Polecenie cmdlet **Start-AzStorageBlobCopy** rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="90f26-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="90f26-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90f26-117">EXAMPLES</span></span>

### <span data-ttu-id="90f26-118">Przykład 1: kopiowanie nazwanego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="90f26-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="90f26-119">To polecenie uruchamia operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015 z kontenera o nazwie ContosoUploads do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="90f26-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="90f26-120">Przykład 2: Uzyskaj kontener określający obiekty blob do skopiowania</span><span class="sxs-lookup"><span data-stu-id="90f26-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="90f26-121">To polecenie uzyskuje kontener o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzStorageContainer** , a następnie przekazuje kontener do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="90f26-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90f26-122">To polecenie cmdlet rozpoczyna operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="90f26-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="90f26-123">Poprzednie polecenie cmdlet udostępnia kontener źródłowy.</span><span class="sxs-lookup"><span data-stu-id="90f26-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="90f26-124">Parametr *DestContainer* określa ContosoArchives jako kontener docelowy.</span><span class="sxs-lookup"><span data-stu-id="90f26-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="90f26-125">Przykład 3: pobieranie wszystkich obiektów BLOB w kontenerze i ich kopiowanie</span><span class="sxs-lookup"><span data-stu-id="90f26-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="90f26-126">To polecenie pobiera obiekty blob w kontenerze o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzStorageBlob** , a następnie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="90f26-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90f26-127">To polecenie cmdlet rozpoczyna operację kopiowania obiektów BLOB do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="90f26-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="90f26-128">Przykład 4: Kopiowanie obiektu blob określonego jako obiekt</span><span class="sxs-lookup"><span data-stu-id="90f26-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="90f26-129">Pierwsze polecenie uzyskuje obiekt BLOB o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="90f26-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="90f26-130">Polecenie zapisuje ten obiekt w zmiennej $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="90f26-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="90f26-131">Drugie polecenie pobiera obiekt BLOB o nazwie ContosoPlanning2015Archived w kontenerze o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="90f26-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="90f26-132">Polecenie zapisuje ten obiekt w zmiennej $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="90f26-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="90f26-133">Ostatnie polecenie rozpoczyna operację kopiowania z kontenera źródłowego do kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="90f26-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="90f26-134">W poleceniu użyto standardowego zapisu kropkowego do określenia obiektów **ICloudBlob** $SrcBlob i $DestBlob obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="90f26-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="90f26-135">Przykład 5: Kopiowanie obiektu BLOB z identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="90f26-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="90f26-136">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten klucz w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="90f26-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="90f26-137">Drugie polecenie skopiuje plik z określonego identyfikatora URI do obiektu BLOB o nazwie ContosoPlanning w kontenerze o nazwie ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="90f26-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="90f26-138">Polecenie rozpoczyna operację kopiowania w kontekście przechowywanym w $Context.</span><span class="sxs-lookup"><span data-stu-id="90f26-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="90f26-139">Przykład 6: Kopiowanie bloku obiektu BLOB do kontenera docelowego przy użyciu nowej nazwy obiektu BLOB i Ustawianie obiektu BLOB StandardBlobTier jako archiwum, RehydratePriority jako wysoka</span><span class="sxs-lookup"><span data-stu-id="90f26-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Archive
```

<span data-ttu-id="90f26-140">To polecenie uruchamia operację kopiowania bloku docelowego w kontenerze docelowym przy użyciu nowej nazwy obiektu BLOB i ustawia docelowe StandardBlobTier jako archiwum, RehydratePriority jako wysokie</span><span class="sxs-lookup"><span data-stu-id="90f26-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Archive, RehydratePriority as High</span></span>

## <span data-ttu-id="90f26-141">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90f26-141">PARAMETERS</span></span>

### <span data-ttu-id="90f26-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="90f26-142">-AbsoluteUri</span></span>
<span data-ttu-id="90f26-143">Określa bezwzględny identyfikator URI pliku, który ma zostać skopiowany do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="90f26-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="90f26-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90f26-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="90f26-145">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="90f26-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="90f26-146">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="90f26-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="90f26-147">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="90f26-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="90f26-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="90f26-148">-CloudBlob</span></span>
<span data-ttu-id="90f26-149">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90f26-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="90f26-150">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="90f26-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="90f26-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="90f26-151">-CloudBlobContainer</span></span>
<span data-ttu-id="90f26-152">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90f26-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="90f26-153">To polecenie cmdlet umożliwia skopiowanie obiektu BLOB z kontenera, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="90f26-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="90f26-154">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="90f26-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="90f26-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="90f26-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="90f26-156">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="90f26-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="90f26-157">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="90f26-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="90f26-158">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="90f26-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="90f26-159">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="90f26-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="90f26-160">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="90f26-160">The default value is 10.</span></span>

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

### <span data-ttu-id="90f26-161">-Context</span><span class="sxs-lookup"><span data-stu-id="90f26-161">-Context</span></span>
<span data-ttu-id="90f26-162">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="90f26-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90f26-163">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="90f26-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="90f26-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f26-164">-DefaultProfile</span></span>
<span data-ttu-id="90f26-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90f26-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90f26-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="90f26-166">-DestBlob</span></span>
<span data-ttu-id="90f26-167">Określa nazwę docelowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="90f26-167">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="90f26-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="90f26-168">-DestCloudBlob</span></span>
<span data-ttu-id="90f26-169">Określa docelowy obiekt **CloudBlob**</span><span class="sxs-lookup"><span data-stu-id="90f26-169">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="90f26-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="90f26-170">-DestContainer</span></span>
<span data-ttu-id="90f26-171">Określa nazwę kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="90f26-171">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="90f26-172">-DestContext</span><span class="sxs-lookup"><span data-stu-id="90f26-172">-DestContext</span></span>
<span data-ttu-id="90f26-173">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="90f26-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90f26-174">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="90f26-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="90f26-175">-Force</span><span class="sxs-lookup"><span data-stu-id="90f26-175">-Force</span></span>
<span data-ttu-id="90f26-176">Wskazuje, że to polecenie cmdlet zastępuje docelowy obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90f26-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="90f26-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="90f26-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="90f26-178">Warstwa obiektu BLOB strony Premium</span><span class="sxs-lookup"><span data-stu-id="90f26-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f26-179">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="90f26-179">-RehydratePriority</span></span>
<span data-ttu-id="90f26-180">Blokowanie obiektu BLOB RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="90f26-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="90f26-181">Wskazuje priorytet, za pomocą którego można rehydratacji zarchiwizowany obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="90f26-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="90f26-182">Prawidłowe wartości to High/Standard.</span><span class="sxs-lookup"><span data-stu-id="90f26-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f26-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90f26-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="90f26-184">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="90f26-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="90f26-185">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="90f26-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="90f26-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="90f26-186">-SrcBlob</span></span>
<span data-ttu-id="90f26-187">Określa nazwę źródłowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="90f26-187">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="90f26-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="90f26-188">-SrcContainer</span></span>
<span data-ttu-id="90f26-189">Określa nazwę kontenera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="90f26-189">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="90f26-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="90f26-190">-SrcDir</span></span>
<span data-ttu-id="90f26-191">Określa obiekt **CloudFileDirectory** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90f26-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="90f26-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="90f26-192">-SrcFile</span></span>
<span data-ttu-id="90f26-193">Określa obiekt **CloudFile** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90f26-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="90f26-194">Możesz je utworzyć lub użyć Get-AzStorageFile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90f26-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="90f26-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="90f26-195">-SrcFilePath</span></span>
<span data-ttu-id="90f26-196">Określa względną ścieżkę pliku źródłowego katalogu źródłowego lub udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="90f26-196">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="90f26-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="90f26-197">-SrcShare</span></span>
<span data-ttu-id="90f26-198">Określa obiekt **CloudFileShare** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90f26-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="90f26-199">Możesz je utworzyć lub użyć Get-AzStorageShare polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90f26-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="90f26-200">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="90f26-200">-SrcShareName</span></span>
<span data-ttu-id="90f26-201">Określa nazwę udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="90f26-201">Specifies the source share name.</span></span>

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

### <span data-ttu-id="90f26-202">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="90f26-202">-StandardBlobTier</span></span>
<span data-ttu-id="90f26-203">Blokada warstwy obiektu BLOB, prawidłowe wartości to Hot/chłodna/archiwum.</span><span class="sxs-lookup"><span data-stu-id="90f26-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="90f26-204">Zobacz szczegóły https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="90f26-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f26-205">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90f26-205">-Confirm</span></span>
<span data-ttu-id="90f26-206">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90f26-206">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f26-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f26-207">-WhatIf</span></span>
<span data-ttu-id="90f26-208">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90f26-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90f26-209">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90f26-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f26-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f26-210">CommonParameters</span></span>
<span data-ttu-id="90f26-211">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f26-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f26-212">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f26-212">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f26-213">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90f26-213">INPUTS</span></span>

### <span data-ttu-id="90f26-214">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="90f26-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="90f26-215">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="90f26-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="90f26-216">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="90f26-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="90f26-217">System. String</span><span class="sxs-lookup"><span data-stu-id="90f26-217">System.String</span></span>

### <span data-ttu-id="90f26-218">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90f26-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="90f26-219">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90f26-219">OUTPUTS</span></span>

### <span data-ttu-id="90f26-220">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="90f26-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="90f26-221">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90f26-221">NOTES</span></span>

## <span data-ttu-id="90f26-222">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90f26-222">RELATED LINKS</span></span>

[<span data-ttu-id="90f26-223">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="90f26-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="90f26-224">Zatrzymaj — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="90f26-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
