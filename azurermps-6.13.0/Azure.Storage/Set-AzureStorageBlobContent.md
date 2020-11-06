---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageBlobContent.md
ms.openlocfilehash: edc2a178ac8fa1c3a009830decb62d60ece2a367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542080"
---
# <span data-ttu-id="521ff-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="521ff-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="521ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="521ff-102">SYNOPSIS</span></span>
<span data-ttu-id="521ff-103">Wysyła plik lokalny do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="521ff-103">Uploads a local file to an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="521ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="521ff-104">SYNTAX</span></span>

### <span data-ttu-id="521ff-105">SendManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="521ff-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="521ff-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="521ff-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="521ff-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="521ff-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="521ff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="521ff-108">DESCRIPTION</span></span>
<span data-ttu-id="521ff-109">Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazywanie pliku lokalnego do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="521ff-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="521ff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="521ff-110">EXAMPLES</span></span>

### <span data-ttu-id="521ff-111">Przykład 1: przekazywanie nazwanego pliku</span><span class="sxs-lookup"><span data-stu-id="521ff-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="521ff-112">To polecenie przekazuje plik o nazwie PlanningData do obiektu BLOB o nazwie Planning2015.</span><span class="sxs-lookup"><span data-stu-id="521ff-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="521ff-113">Przykład 2: przekazywanie wszystkich plików w folderze bieżącym</span><span class="sxs-lookup"><span data-stu-id="521ff-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="521ff-114">To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem do pobierania wszystkich plików w bieżącym folderze i podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="521ff-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="521ff-115">Polecenie cmdlet **Set-AzureStorageBlobContent** umożliwia przekazanie plików do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="521ff-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="521ff-116">Przykład 3: zastąpienie istniejącego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="521ff-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="521ff-117">To polecenie uzyskuje obiekt BLOB o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzureStorageBlob, a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="521ff-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="521ff-118">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="521ff-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="521ff-119">To polecenie nie określa parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="521ff-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="521ff-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="521ff-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="521ff-121">Jeśli potwierdzisz polecenie, polecenie cmdlet zastąpi istniejący obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="521ff-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="521ff-122">Przykład 4: przekazywanie pliku do kontenera przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="521ff-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="521ff-123">To polecenie uzyskuje kontener, który zaczyna się od ciągu ContosoUpload, przy użyciu polecenia cmdlet **Get-AzureStorageContainer** , a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="521ff-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="521ff-124">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="521ff-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="521ff-125">Przykład 5: przekazywanie pliku do obiektu BLOB strony za pomocą metadanych i PremiumPageBlobTier jako P10</span><span class="sxs-lookup"><span data-stu-id="521ff-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="521ff-126">Pierwsze polecenie tworzy tabelę skrótów zawierającą metadane dla obiektu BLOB i zapisuje tę tabelę w zmiennej $Metadata.</span><span class="sxs-lookup"><span data-stu-id="521ff-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="521ff-127">Drugie polecenie przekazuje plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="521ff-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="521ff-128">Obiekt BLOB zawiera metadane przechowywane w $Metadata i ma PremiumPageBlobTier jako P10.</span><span class="sxs-lookup"><span data-stu-id="521ff-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="521ff-129">Przykład 6: przekazywanie pliku do obiektu BLOB przy użyciu określonych właściwości obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="521ff-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="521ff-130">To polecenie wysyła plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads z określonymi właściwościami obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="521ff-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="521ff-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="521ff-131">PARAMETERS</span></span>

### <span data-ttu-id="521ff-132">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="521ff-132">-Blob</span></span>
<span data-ttu-id="521ff-133">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="521ff-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="521ff-134">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="521ff-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-135">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="521ff-135">-BlobType</span></span>
<span data-ttu-id="521ff-136">Określa typ obiektu BLOB, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="521ff-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="521ff-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="521ff-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="521ff-138">Drukowany</span><span class="sxs-lookup"><span data-stu-id="521ff-138">Block</span></span>
- <span data-ttu-id="521ff-139">Strona wartość domyślna to Block.</span><span class="sxs-lookup"><span data-stu-id="521ff-139">Page The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-140">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="521ff-140">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="521ff-141">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="521ff-141">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="521ff-142">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="521ff-142">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="521ff-143">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="521ff-143">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="521ff-144">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="521ff-144">-CloudBlob</span></span>
<span data-ttu-id="521ff-145">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="521ff-145">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="521ff-146">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="521ff-146">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-147">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="521ff-147">-CloudBlobContainer</span></span>
<span data-ttu-id="521ff-148">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="521ff-148">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="521ff-149">To polecenie cmdlet umożliwia przekazywanie zawartości do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="521ff-149">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="521ff-150">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="521ff-150">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-151">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="521ff-151">-ConcurrentTaskCount</span></span>
<span data-ttu-id="521ff-152">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="521ff-152">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="521ff-153">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="521ff-153">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="521ff-154">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="521ff-154">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="521ff-155">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="521ff-155">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="521ff-156">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="521ff-156">The default value is 10.</span></span>

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

### <span data-ttu-id="521ff-157">-Kontener</span><span class="sxs-lookup"><span data-stu-id="521ff-157">-Container</span></span>
<span data-ttu-id="521ff-158">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="521ff-158">Specifies the name of a container.</span></span>
<span data-ttu-id="521ff-159">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="521ff-159">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-160">-Context</span><span class="sxs-lookup"><span data-stu-id="521ff-160">-Context</span></span>
<span data-ttu-id="521ff-161">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="521ff-161">Specifies an Azure storage context.</span></span>
<span data-ttu-id="521ff-162">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="521ff-162">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="521ff-163">Aby użyć kontekstu magazynu utworzonego na podstawie tokenu SAS bez uprawnienia do odczytu, należy dodać parametr Force, aby pominąć obiekt BLOB Check.</span><span class="sxs-lookup"><span data-stu-id="521ff-163">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521ff-164">-DefaultProfile</span></span>
<span data-ttu-id="521ff-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="521ff-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-166">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="521ff-166">-File</span></span>
<span data-ttu-id="521ff-167">Określa lokalną ścieżkę do pliku, który ma zostać przekazany jako zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="521ff-167">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-168">-Force</span><span class="sxs-lookup"><span data-stu-id="521ff-168">-Force</span></span>
<span data-ttu-id="521ff-169">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="521ff-169">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="521ff-170">-Metadata</span><span class="sxs-lookup"><span data-stu-id="521ff-170">-Metadata</span></span>
<span data-ttu-id="521ff-171">Określa metadane przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="521ff-171">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-172">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="521ff-172">-PremiumPageBlobTier</span></span>
<span data-ttu-id="521ff-173">Warstwa obiektu BLOB strony</span><span class="sxs-lookup"><span data-stu-id="521ff-173">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-174">-Properties</span><span class="sxs-lookup"><span data-stu-id="521ff-174">-Properties</span></span>
<span data-ttu-id="521ff-175">Określa właściwości przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="521ff-175">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="521ff-176">Obsługiwane właściwości to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="521ff-176">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="521ff-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="521ff-178">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="521ff-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="521ff-179">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="521ff-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="521ff-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="521ff-180">-Confirm</span></span>
<span data-ttu-id="521ff-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="521ff-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="521ff-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="521ff-182">-WhatIf</span></span>
<span data-ttu-id="521ff-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="521ff-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="521ff-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="521ff-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="521ff-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521ff-185">CommonParameters</span></span>
<span data-ttu-id="521ff-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521ff-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521ff-187">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521ff-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521ff-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="521ff-188">INPUTS</span></span>

### <span data-ttu-id="521ff-189">System. String</span><span class="sxs-lookup"><span data-stu-id="521ff-189">System.String</span></span>

### <span data-ttu-id="521ff-190">Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="521ff-190">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="521ff-191">Microsoft. platformy windowsazure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="521ff-191">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="521ff-192">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="521ff-192">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="521ff-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="521ff-193">OUTPUTS</span></span>

### <span data-ttu-id="521ff-194">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="521ff-194">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="521ff-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="521ff-195">NOTES</span></span>

## <span data-ttu-id="521ff-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="521ff-196">RELATED LINKS</span></span>

[<span data-ttu-id="521ff-197">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="521ff-197">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="521ff-198">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="521ff-198">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="521ff-199">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="521ff-199">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
