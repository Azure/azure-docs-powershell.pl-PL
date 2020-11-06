---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523910"
---
# <span data-ttu-id="b7966-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b7966-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="b7966-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7966-102">SYNOPSIS</span></span>
<span data-ttu-id="b7966-103">Wysyła plik lokalny do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b7966-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="b7966-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7966-104">SYNTAX</span></span>

### <span data-ttu-id="b7966-105">SendManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7966-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7966-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b7966-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7966-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b7966-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7966-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b7966-108">DESCRIPTION</span></span>
<span data-ttu-id="b7966-109">Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazywanie pliku lokalnego do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b7966-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="b7966-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7966-110">EXAMPLES</span></span>

### <span data-ttu-id="b7966-111">Przykład 1: przekazywanie nazwanego pliku</span><span class="sxs-lookup"><span data-stu-id="b7966-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="b7966-112">To polecenie przekazuje plik o nazwie PlanningData do obiektu BLOB o nazwie Planning2015.</span><span class="sxs-lookup"><span data-stu-id="b7966-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="b7966-113">Przykład 2: przekazywanie wszystkich plików w folderze bieżącym</span><span class="sxs-lookup"><span data-stu-id="b7966-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="b7966-114">To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem do pobierania wszystkich plików w bieżącym folderze i podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b7966-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b7966-115">Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazanie plików do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="b7966-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="b7966-116">Przykład 3: zastąpienie istniejącego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="b7966-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="b7966-117">To polecenie uzyskuje obiekt BLOB o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzureStorageBlob, a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7966-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="b7966-118">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="b7966-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="b7966-119">To polecenie nie określa parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="b7966-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="b7966-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b7966-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="b7966-121">Jeśli potwierdzisz polecenie, polecenie cmdlet zastąpi istniejący obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7966-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="b7966-122">Przykład 4: przekazywanie pliku do kontenera przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="b7966-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="b7966-123">To polecenie uzyskuje kontener, który zaczyna się od ciągu ContosoUpload, przy użyciu polecenia cmdlet **Get-AzureStorageContainer** , a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7966-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="b7966-124">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="b7966-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="b7966-125">Przykład 5: przekazywanie pliku i metadanych</span><span class="sxs-lookup"><span data-stu-id="b7966-125">Example 5: Upload a file and metadata</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

<span data-ttu-id="b7966-126">Pierwsze polecenie tworzy tabelę skrótów zawierającą metadane dla obiektu BLOB i zapisuje tę tabelę w zmiennej $Metadata.</span><span class="sxs-lookup"><span data-stu-id="b7966-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="b7966-127">Drugie polecenie przekazuje plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="b7966-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="b7966-128">Obiekt BLOB zawiera metadane przechowywane w $Metadata.</span><span class="sxs-lookup"><span data-stu-id="b7966-128">The blob includes the metadata stored in $Metadata.</span></span>

## <span data-ttu-id="b7966-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7966-129">PARAMETERS</span></span>

### <span data-ttu-id="b7966-130">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="b7966-130">-Blob</span></span>
<span data-ttu-id="b7966-131">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7966-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="b7966-132">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b7966-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7966-133">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="b7966-133">-BlobType</span></span>
<span data-ttu-id="b7966-134">Określa typ obiektu BLOB, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7966-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="b7966-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b7966-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7966-136">Drukowany</span><span class="sxs-lookup"><span data-stu-id="b7966-136">Block</span></span>
- <span data-ttu-id="b7966-137">Stronic</span><span class="sxs-lookup"><span data-stu-id="b7966-137">Page</span></span>

<span data-ttu-id="b7966-138">Wartość domyślna to Block.</span><span class="sxs-lookup"><span data-stu-id="b7966-138">The default value is Block.</span></span>

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

### <span data-ttu-id="b7966-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7966-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b7966-140">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b7966-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b7966-141">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="b7966-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b7966-142">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="b7966-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b7966-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b7966-143">-CloudBlob</span></span>
<span data-ttu-id="b7966-144">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="b7966-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="b7966-145">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="b7966-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b7966-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b7966-146">-CloudBlobContainer</span></span>
<span data-ttu-id="b7966-147">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b7966-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b7966-148">To polecenie cmdlet umożliwia przekazywanie zawartości do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b7966-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="b7966-149">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="b7966-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b7966-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b7966-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b7966-151">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b7966-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b7966-152">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b7966-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b7966-153">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="b7966-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b7966-154">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b7966-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b7966-155">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b7966-155">The default value is 10.</span></span>

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

### <span data-ttu-id="b7966-156">-Kontener</span><span class="sxs-lookup"><span data-stu-id="b7966-156">-Container</span></span>
<span data-ttu-id="b7966-157">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="b7966-157">Specifies the name of a container.</span></span>
<span data-ttu-id="b7966-158">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b7966-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7966-159">-Context</span><span class="sxs-lookup"><span data-stu-id="b7966-159">-Context</span></span>
<span data-ttu-id="b7966-160">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b7966-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b7966-161">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b7966-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b7966-162">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="b7966-162">-File</span></span>
<span data-ttu-id="b7966-163">Określa lokalną ścieżkę do pliku, który ma zostać przekazany jako zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7966-163">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="b7966-164">-Force</span><span class="sxs-lookup"><span data-stu-id="b7966-164">-Force</span></span>
<span data-ttu-id="b7966-165">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b7966-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b7966-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b7966-166">-Metadata</span></span>
<span data-ttu-id="b7966-167">Określa metadane przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7966-167">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="b7966-168">-Properties</span><span class="sxs-lookup"><span data-stu-id="b7966-168">-Properties</span></span>
<span data-ttu-id="b7966-169">Określa właściwości przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7966-169">Specifies properties for the uploaded blob.</span></span>

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

### <span data-ttu-id="b7966-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7966-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b7966-171">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="b7966-171">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b7966-172">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="b7966-172">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b7966-173">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7966-173">-Confirm</span></span>
<span data-ttu-id="b7966-174">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7966-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7966-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7966-175">-WhatIf</span></span>
<span data-ttu-id="b7966-176">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7966-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7966-177">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7966-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7966-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7966-178">CommonParameters</span></span>
<span data-ttu-id="b7966-179">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7966-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7966-180">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7966-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7966-181">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7966-181">INPUTS</span></span>

## <span data-ttu-id="b7966-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7966-182">OUTPUTS</span></span>

## <span data-ttu-id="b7966-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7966-183">NOTES</span></span>

## <span data-ttu-id="b7966-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7966-184">RELATED LINKS</span></span>

[<span data-ttu-id="b7966-185">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b7966-185">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="b7966-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b7966-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="b7966-187">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b7966-187">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
