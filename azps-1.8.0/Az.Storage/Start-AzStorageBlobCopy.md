---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: e83d86b770208afb62398ed797b3763424bbd07f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707490"
---
# <span data-ttu-id="3bc5f-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3bc5f-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="3bc5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc5f-103">Rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="3bc5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bc5f-104">SYNTAX</span></span>

### <span data-ttu-id="3bc5f-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3bc5f-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="3bc5f-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="3bc5f-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3bc5f-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-109">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="3bc5f-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="3bc5f-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="3bc5f-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="3bc5f-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="3bc5f-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc5f-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="3bc5f-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc5f-115">Opis</span><span class="sxs-lookup"><span data-stu-id="3bc5f-115">DESCRIPTION</span></span>
<span data-ttu-id="3bc5f-116">Polecenie cmdlet **Start-AzStorageBlobCopy** rozpoczyna Kopiowanie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="3bc5f-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bc5f-117">EXAMPLES</span></span>

### <span data-ttu-id="3bc5f-118">Przykład 1: kopiowanie nazwanego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="3bc5f-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="3bc5f-119">To polecenie uruchamia operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015 z kontenera o nazwie ContosoUploads do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="3bc5f-120">Przykład 2: Uzyskaj kontener określający obiekty blob do skopiowania</span><span class="sxs-lookup"><span data-stu-id="3bc5f-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="3bc5f-121">To polecenie uzyskuje kontener o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzStorageContainer** , a następnie przekazuje kontener do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3bc5f-122">To polecenie cmdlet rozpoczyna operację kopiowania obiektu BLOB o nazwie ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="3bc5f-123">Poprzednie polecenie cmdlet udostępnia kontener źródłowy.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="3bc5f-124">Parametr *DestContainer* określa ContosoArchives jako kontener docelowy.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="3bc5f-125">Przykład 3: pobieranie wszystkich obiektów BLOB w kontenerze i ich kopiowanie</span><span class="sxs-lookup"><span data-stu-id="3bc5f-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="3bc5f-126">To polecenie pobiera obiekty blob w kontenerze o nazwie ContosoUploads, używając polecenia cmdlet **Get-AzStorageBlob** , a następnie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3bc5f-127">To polecenie cmdlet rozpoczyna operację kopiowania obiektów BLOB do kontenera o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="3bc5f-128">Przykład 4: Kopiowanie obiektu blob określonego jako obiekt</span><span class="sxs-lookup"><span data-stu-id="3bc5f-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="3bc5f-129">Pierwsze polecenie uzyskuje obiekt BLOB o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="3bc5f-130">Polecenie zapisuje ten obiekt w zmiennej $SrcBlob.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="3bc5f-131">Drugie polecenie pobiera obiekt BLOB o nazwie ContosoPlanning2015Archived w kontenerze o nazwie ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="3bc5f-132">Polecenie zapisuje ten obiekt w zmiennej $DestBlob.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="3bc5f-133">Ostatnie polecenie rozpoczyna operację kopiowania z kontenera źródłowego do kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="3bc5f-134">W poleceniu użyto standardowego zapisu kropkowego do określenia obiektów **ICloudBlob** $SrcBlob i $DestBlob obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="3bc5f-135">Przykład 5: Kopiowanie obiektu BLOB z identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="3bc5f-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="3bc5f-136">To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten klucz w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="3bc5f-137">Drugie polecenie skopiuje plik z określonego identyfikatora URI do obiektu BLOB o nazwie ContosoPlanning w kontenerze o nazwie ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="3bc5f-138">Polecenie rozpoczyna operację kopiowania w kontekście przechowywanym w $Context.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="3bc5f-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bc5f-139">PARAMETERS</span></span>

### <span data-ttu-id="3bc5f-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="3bc5f-140">-AbsoluteUri</span></span>
<span data-ttu-id="3bc5f-141">Określa bezwzględny identyfikator URI pliku, który ma zostać skopiowany do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="3bc5f-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bc5f-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3bc5f-143">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3bc5f-144">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3bc5f-145">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3bc5f-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3bc5f-146">-CloudBlob</span></span>
<span data-ttu-id="3bc5f-147">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3bc5f-148">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc5f-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3bc5f-149">-CloudBlobContainer</span></span>
<span data-ttu-id="3bc5f-150">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="3bc5f-151">To polecenie cmdlet umożliwia skopiowanie obiektu BLOB z kontenera, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="3bc5f-152">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="3bc5f-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3bc5f-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3bc5f-154">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3bc5f-155">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3bc5f-156">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3bc5f-157">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3bc5f-158">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-158">The default value is 10.</span></span>

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

### <span data-ttu-id="3bc5f-159">-Context</span><span class="sxs-lookup"><span data-stu-id="3bc5f-159">-Context</span></span>
<span data-ttu-id="3bc5f-160">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3bc5f-161">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-161">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3bc5f-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc5f-162">-DefaultProfile</span></span>
<span data-ttu-id="3bc5f-163">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc5f-164">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="3bc5f-164">-DestBlob</span></span>
<span data-ttu-id="3bc5f-165">Określa nazwę docelowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-165">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="3bc5f-166">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="3bc5f-166">-DestCloudBlob</span></span>
<span data-ttu-id="3bc5f-167">Określa docelowy obiekt **CloudBlob**</span><span class="sxs-lookup"><span data-stu-id="3bc5f-167">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc5f-168">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="3bc5f-168">-DestContainer</span></span>
<span data-ttu-id="3bc5f-169">Określa nazwę kontenera docelowego.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-169">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="3bc5f-170">-DestContext</span><span class="sxs-lookup"><span data-stu-id="3bc5f-170">-DestContext</span></span>
<span data-ttu-id="3bc5f-171">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-171">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3bc5f-172">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-172">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3bc5f-173">-Force</span><span class="sxs-lookup"><span data-stu-id="3bc5f-173">-Force</span></span>
<span data-ttu-id="3bc5f-174">Wskazuje, że to polecenie cmdlet zastępuje docelowy obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-174">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3bc5f-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="3bc5f-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="3bc5f-176">Warstwa obiektu BLOB strony Premium</span><span class="sxs-lookup"><span data-stu-id="3bc5f-176">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc5f-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bc5f-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3bc5f-178">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3bc5f-179">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3bc5f-180">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="3bc5f-180">-SrcBlob</span></span>
<span data-ttu-id="3bc5f-181">Określa nazwę źródłowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-181">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="3bc5f-182">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="3bc5f-182">-SrcContainer</span></span>
<span data-ttu-id="3bc5f-183">Określa nazwę kontenera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-183">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="3bc5f-184">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="3bc5f-184">-SrcDir</span></span>
<span data-ttu-id="3bc5f-185">Określa obiekt **CloudFileDirectory** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-185">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc5f-186">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="3bc5f-186">-SrcFile</span></span>
<span data-ttu-id="3bc5f-187">Specifes obiekt **CloudFile** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-187">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3bc5f-188">Możesz je utworzyć lub użyć Get-AzStorageFile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-188">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc5f-189">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="3bc5f-189">-SrcFilePath</span></span>
<span data-ttu-id="3bc5f-190">Określa względną ścieżkę pliku źródłowego katalogu źródłowego lub udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-190">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="3bc5f-191">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="3bc5f-191">-SrcShare</span></span>
<span data-ttu-id="3bc5f-192">Określa obiekt **CloudFileShare** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-192">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3bc5f-193">Możesz je utworzyć lub użyć Get-AzStorageShare polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-193">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc5f-194">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="3bc5f-194">-SrcShareName</span></span>
<span data-ttu-id="3bc5f-195">Określa nazwę udziału źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-195">Specifies the source share name.</span></span>

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

### <span data-ttu-id="3bc5f-196">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bc5f-196">-Confirm</span></span>
<span data-ttu-id="3bc5f-197">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc5f-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc5f-198">-WhatIf</span></span>
<span data-ttu-id="3bc5f-199">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc5f-200">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc5f-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc5f-201">CommonParameters</span></span>
<span data-ttu-id="3bc5f-202">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc5f-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc5f-203">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc5f-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc5f-204">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bc5f-204">INPUTS</span></span>

### <span data-ttu-id="3bc5f-205">Microsoft. platformy windowsazure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3bc5f-205">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="3bc5f-206">Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3bc5f-206">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="3bc5f-207">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3bc5f-207">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3bc5f-208">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc5f-208">System.String</span></span>

### <span data-ttu-id="3bc5f-209">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bc5f-209">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3bc5f-210">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bc5f-210">OUTPUTS</span></span>

### <span data-ttu-id="3bc5f-211">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3bc5f-211">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="3bc5f-212">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bc5f-212">NOTES</span></span>

## <span data-ttu-id="3bc5f-213">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bc5f-213">RELATED LINKS</span></span>

[<span data-ttu-id="3bc5f-214">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="3bc5f-214">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="3bc5f-215">Zatrzymaj — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3bc5f-215">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
