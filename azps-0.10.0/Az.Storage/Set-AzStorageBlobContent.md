---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 0730d509ddf207d7541e854b15f34c30b44093e0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892045"
---
# <span data-ttu-id="7f6d9-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7f6d9-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="7f6d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6d9-103">Wysyła plik lokalny do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="7f6d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f6d9-104">SYNTAX</span></span>

### <span data-ttu-id="7f6d9-105">SendManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f6d9-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f6d9-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="7f6d9-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f6d9-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="7f6d9-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f6d9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7f6d9-108">DESCRIPTION</span></span>
<span data-ttu-id="7f6d9-109">Polecenie cmdlet **Set-AzStorageBlobContent** umożliwia przekazywanie pliku lokalnego do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="7f6d9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f6d9-110">EXAMPLES</span></span>

### <span data-ttu-id="7f6d9-111">Przykład 1: przekazywanie nazwanego pliku</span><span class="sxs-lookup"><span data-stu-id="7f6d9-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="7f6d9-112">To polecenie przekazuje plik o nazwie PlanningData do obiektu BLOB o nazwie Planning2015.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="7f6d9-113">Przykład 2: przekazywanie wszystkich plików w folderze bieżącym</span><span class="sxs-lookup"><span data-stu-id="7f6d9-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="7f6d9-114">To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem do pobierania wszystkich plików w bieżącym folderze i podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7f6d9-115">Polecenie cmdlet **Set-AzStorageBlobContent** umożliwia przekazanie plików do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="7f6d9-116">Przykład 3: zastąpienie istniejącego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="7f6d9-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="7f6d9-117">To polecenie uzyskuje obiekt BLOB o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzStorageBlob, a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="7f6d9-118">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="7f6d9-119">To polecenie nie określa parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="7f6d9-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="7f6d9-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="7f6d9-121">Jeśli potwierdzisz polecenie, polecenie cmdlet zastąpi istniejący obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="7f6d9-122">Przykład 4: przekazywanie pliku do kontenera przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="7f6d9-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="7f6d9-123">To polecenie uzyskuje kontener, który zaczyna się od ciągu ContosoUpload, przy użyciu polecenia cmdlet **Get-AzStorageContainer** , a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="7f6d9-124">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="7f6d9-125">Przykład 5: przekazywanie pliku do obiektu BLOB strony za pomocą metadanych i PremiumPageBlobTier jako P10</span><span class="sxs-lookup"><span data-stu-id="7f6d9-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="7f6d9-126">Pierwsze polecenie tworzy tabelę skrótów zawierającą metadane dla obiektu BLOB i zapisuje tę tabelę w zmiennej $Metadata.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="7f6d9-127">Drugie polecenie przekazuje plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="7f6d9-128">Obiekt BLOB zawiera metadane przechowywane w $Metadata i ma PremiumPageBlobTier jako P10.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="7f6d9-129">Przykład 6: przekazywanie pliku do obiektu BLOB przy użyciu określonych właściwości obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="7f6d9-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="7f6d9-130">To polecenie wysyła plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads z określonymi właściwościami obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="7f6d9-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f6d9-131">PARAMETERS</span></span>

### <span data-ttu-id="7f6d9-132">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="7f6d9-132">-Blob</span></span>
<span data-ttu-id="7f6d9-133">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="7f6d9-134">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f6d9-135">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="7f6d9-135">-BlobType</span></span>
<span data-ttu-id="7f6d9-136">Określa typ obiektu BLOB, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="7f6d9-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7f6d9-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f6d9-138">Drukowany</span><span class="sxs-lookup"><span data-stu-id="7f6d9-138">Block</span></span>
- <span data-ttu-id="7f6d9-139">Strona wartość domyślna to Block.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-139">Page The default value is Block.</span></span>

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

### <span data-ttu-id="7f6d9-140">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7f6d9-140">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7f6d9-141">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-141">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7f6d9-142">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-142">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7f6d9-143">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-143">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7f6d9-144">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7f6d9-144">-CloudBlob</span></span>
<span data-ttu-id="7f6d9-145">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="7f6d9-145">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="7f6d9-146">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-146">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6d9-147">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7f6d9-147">-CloudBlobContainer</span></span>
<span data-ttu-id="7f6d9-148">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-148">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="7f6d9-149">To polecenie cmdlet umożliwia przekazywanie zawartości do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-149">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="7f6d9-150">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-150">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6d9-151">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7f6d9-151">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7f6d9-152">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-152">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7f6d9-153">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-153">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7f6d9-154">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-154">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7f6d9-155">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-155">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7f6d9-156">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-156">The default value is 10.</span></span>

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

### <span data-ttu-id="7f6d9-157">-Kontener</span><span class="sxs-lookup"><span data-stu-id="7f6d9-157">-Container</span></span>
<span data-ttu-id="7f6d9-158">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-158">Specifies the name of a container.</span></span>
<span data-ttu-id="7f6d9-159">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-159">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f6d9-160">-Context</span><span class="sxs-lookup"><span data-stu-id="7f6d9-160">-Context</span></span>
<span data-ttu-id="7f6d9-161">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-161">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7f6d9-162">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-162">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7f6d9-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6d9-163">-DefaultProfile</span></span>
<span data-ttu-id="7f6d9-164">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-164">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f6d9-165">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="7f6d9-165">-File</span></span>
<span data-ttu-id="7f6d9-166">Określa lokalną ścieżkę do pliku, który ma zostać przekazany jako zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-166">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="7f6d9-167">-Force</span><span class="sxs-lookup"><span data-stu-id="7f6d9-167">-Force</span></span>
<span data-ttu-id="7f6d9-168">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-168">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7f6d9-169">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7f6d9-169">-Metadata</span></span>
<span data-ttu-id="7f6d9-170">Określa metadane przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-170">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="7f6d9-171">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="7f6d9-171">-PremiumPageBlobTier</span></span>
<span data-ttu-id="7f6d9-172">Warstwa obiektu BLOB strony</span><span class="sxs-lookup"><span data-stu-id="7f6d9-172">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f6d9-173">-Properties</span><span class="sxs-lookup"><span data-stu-id="7f6d9-173">-Properties</span></span>
<span data-ttu-id="7f6d9-174">Określa właściwości przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-174">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="7f6d9-175">Obsługiwane właściwości to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-175">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="7f6d9-176">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7f6d9-176">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7f6d9-177">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-177">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7f6d9-178">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-178">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7f6d9-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f6d9-179">-Confirm</span></span>
<span data-ttu-id="7f6d9-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f6d9-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f6d9-181">-WhatIf</span></span>
<span data-ttu-id="7f6d9-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f6d9-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f6d9-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6d9-184">CommonParameters</span></span>
<span data-ttu-id="7f6d9-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6d9-186">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6d9-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6d9-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f6d9-187">INPUTS</span></span>

### <span data-ttu-id="7f6d9-188">System. String</span><span class="sxs-lookup"><span data-stu-id="7f6d9-188">System.String</span></span>

### <span data-ttu-id="7f6d9-189">Microsoft. WindowsAz. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7f6d9-189">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="7f6d9-190">Microsoft. WindowsAz. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7f6d9-190">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="7f6d9-191">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7f6d9-191">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7f6d9-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f6d9-192">OUTPUTS</span></span>

### <span data-ttu-id="7f6d9-193">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7f6d9-193">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="7f6d9-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f6d9-194">NOTES</span></span>

## <span data-ttu-id="7f6d9-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f6d9-195">RELATED LINKS</span></span>

[<span data-ttu-id="7f6d9-196">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7f6d9-196">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="7f6d9-197">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7f6d9-197">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="7f6d9-198">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7f6d9-198">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
