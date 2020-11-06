---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: eddc442dd442fbb64f7b075f49a3c638ea6920e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549052"
---
# <span data-ttu-id="b1b75-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b1b75-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="b1b75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1b75-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b75-103">Wysyła plik lokalny do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b1b75-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1b75-104">SYNTAX</span></span>

### <span data-ttu-id="b1b75-105">SendManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b1b75-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b75-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b1b75-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b75-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b1b75-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b75-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1b75-108">DESCRIPTION</span></span>
<span data-ttu-id="b1b75-109">Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazywanie pliku lokalnego do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b1b75-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="b1b75-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1b75-110">EXAMPLES</span></span>

### <span data-ttu-id="b1b75-111">Przykład 1: przekazywanie nazwanego pliku</span><span class="sxs-lookup"><span data-stu-id="b1b75-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="b1b75-112">To polecenie przekazuje plik o nazwie PlanningData do obiektu BLOB o nazwie Planning2015.</span><span class="sxs-lookup"><span data-stu-id="b1b75-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="b1b75-113">Przykład 2: przekazywanie wszystkich plików w folderze bieżącym</span><span class="sxs-lookup"><span data-stu-id="b1b75-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="b1b75-114">To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem do pobierania wszystkich plików w bieżącym folderze i podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b1b75-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1b75-115">Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazanie plików do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="b1b75-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="b1b75-116">Przykład 3: zastąpienie istniejącego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="b1b75-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="b1b75-117">To polecenie uzyskuje obiekt BLOB o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzureStorageBlob, a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b75-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="b1b75-118">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="b1b75-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="b1b75-119">To polecenie nie określa parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="b1b75-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="b1b75-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b1b75-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="b1b75-121">Jeśli potwierdzisz polecenie, polecenie cmdlet zastąpi istniejący obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="b1b75-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="b1b75-122">Przykład 4: przekazywanie pliku do kontenera przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="b1b75-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="b1b75-123">To polecenie uzyskuje kontener, który zaczyna się od ciągu ContosoUpload, przy użyciu polecenia cmdlet **Get-AzureStorageContainer** , a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b75-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="b1b75-124">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="b1b75-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="b1b75-125">Przykład 5: przekazywanie pliku do obiektu BLOB strony za pomocą metadanych i PremiumPageBlobTier jako P10</span><span class="sxs-lookup"><span data-stu-id="b1b75-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="b1b75-126">Pierwsze polecenie tworzy tabelę skrótów zawierającą metadane dla obiektu BLOB i zapisuje tę tabelę w zmiennej $Metadata.</span><span class="sxs-lookup"><span data-stu-id="b1b75-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="b1b75-127">Drugie polecenie przekazuje plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="b1b75-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="b1b75-128">Obiekt BLOB zawiera metadane przechowywane w $Metadata i ma PremiumPageBlobTier jako P10.</span><span class="sxs-lookup"><span data-stu-id="b1b75-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="b1b75-129">Przykład 6: przekazywanie pliku do obiektu BLOB przy użyciu określonych właściwości obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="b1b75-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="b1b75-130">To polecenie wysyła plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads z określonymi właściwościami obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b1b75-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="b1b75-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1b75-131">PARAMETERS</span></span>

### <span data-ttu-id="b1b75-132">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="b1b75-132">-Blob</span></span>
<span data-ttu-id="b1b75-133">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b1b75-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="b1b75-134">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b1b75-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b75-135">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="b1b75-135">-BlobType</span></span>
<span data-ttu-id="b1b75-136">Określa typ obiektu BLOB, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b75-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="b1b75-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b1b75-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1b75-138">Drukowany</span><span class="sxs-lookup"><span data-stu-id="b1b75-138">Block</span></span>
- <span data-ttu-id="b1b75-139">Stronic</span><span class="sxs-lookup"><span data-stu-id="b1b75-139">Page</span></span>

<span data-ttu-id="b1b75-140">Wartość domyślna to Block.</span><span class="sxs-lookup"><span data-stu-id="b1b75-140">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b75-141">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b1b75-141">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b1b75-142">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b1b75-142">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b1b75-143">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="b1b75-143">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b1b75-144">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="b1b75-144">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b1b75-145">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b1b75-145">-CloudBlob</span></span>
<span data-ttu-id="b1b75-146">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="b1b75-146">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="b1b75-147">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="b1b75-147">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b1b75-148">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b1b75-148">-CloudBlobContainer</span></span>
<span data-ttu-id="b1b75-149">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b75-149">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b1b75-150">To polecenie cmdlet umożliwia przekazywanie zawartości do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b1b75-150">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="b1b75-151">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="b1b75-151">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b1b75-152">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b1b75-152">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b1b75-153">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b1b75-153">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b1b75-154">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b1b75-154">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b1b75-155">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="b1b75-155">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b1b75-156">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b1b75-156">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b1b75-157">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b1b75-157">The default value is 10.</span></span>

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

### <span data-ttu-id="b1b75-158">-Kontener</span><span class="sxs-lookup"><span data-stu-id="b1b75-158">-Container</span></span>
<span data-ttu-id="b1b75-159">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="b1b75-159">Specifies the name of a container.</span></span>
<span data-ttu-id="b1b75-160">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b1b75-160">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b75-161">-Context</span><span class="sxs-lookup"><span data-stu-id="b1b75-161">-Context</span></span>
<span data-ttu-id="b1b75-162">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b1b75-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b1b75-163">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b1b75-163">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b1b75-164">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="b1b75-164">-File</span></span>
<span data-ttu-id="b1b75-165">Określa lokalną ścieżkę do pliku, który ma zostać przekazany jako zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b1b75-165">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b75-166">-Force</span><span class="sxs-lookup"><span data-stu-id="b1b75-166">-Force</span></span>
<span data-ttu-id="b1b75-167">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b1b75-167">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b1b75-168">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b1b75-168">-Metadata</span></span>
<span data-ttu-id="b1b75-169">Określa metadane przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b1b75-169">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b75-170">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="b1b75-170">-PremiumPageBlobTier</span></span>
<span data-ttu-id="b1b75-171">Warstwa obiektu BLOB strony</span><span class="sxs-lookup"><span data-stu-id="b1b75-171">Page Blob Tier</span></span>

```yaml
Type: PremiumPageBlobTier
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b75-172">-Properties</span><span class="sxs-lookup"><span data-stu-id="b1b75-172">-Properties</span></span>
<span data-ttu-id="b1b75-173">Określa właściwości przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b1b75-173">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="b1b75-174">Obsługiwane właściwości to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="b1b75-174">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b75-175">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b1b75-175">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b1b75-176">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="b1b75-176">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b1b75-177">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="b1b75-177">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b1b75-178">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1b75-178">-Confirm</span></span>
<span data-ttu-id="b1b75-179">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b75-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b75-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b75-180">-WhatIf</span></span>
<span data-ttu-id="b1b75-181">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b75-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1b75-182">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1b75-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b75-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b75-183">CommonParameters</span></span>
<span data-ttu-id="b1b75-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b75-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b75-185">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b75-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b75-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1b75-186">INPUTS</span></span>

### <span data-ttu-id="b1b75-187">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b1b75-187">IStorageContext</span></span>

<span data-ttu-id="b1b75-188">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="b1b75-188">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="b1b75-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1b75-189">OUTPUTS</span></span>

### <span data-ttu-id="b1b75-190">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b1b75-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b1b75-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1b75-191">NOTES</span></span>

## <span data-ttu-id="b1b75-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1b75-192">RELATED LINKS</span></span>

[<span data-ttu-id="b1b75-193">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b1b75-193">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="b1b75-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b1b75-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="b1b75-195">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b1b75-195">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
