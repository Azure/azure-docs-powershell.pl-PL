---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 4f29cf8075160e44fb50d838094ef52f9611e0b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704815"
---
# <span data-ttu-id="c509d-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c509d-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="c509d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c509d-102">SYNOPSIS</span></span>
<span data-ttu-id="c509d-103">Wysyła plik lokalny do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c509d-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="c509d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c509d-104">SYNTAX</span></span>

### <span data-ttu-id="c509d-105">SendManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c509d-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c509d-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="c509d-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c509d-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="c509d-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c509d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c509d-108">DESCRIPTION</span></span>
<span data-ttu-id="c509d-109">Polecenie cmdlet **Set-AzStorageBlobContent** umożliwia przekazywanie pliku lokalnego do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c509d-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="c509d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c509d-110">EXAMPLES</span></span>

### <span data-ttu-id="c509d-111">Przykład 1: przekazywanie nazwanego pliku</span><span class="sxs-lookup"><span data-stu-id="c509d-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="c509d-112">To polecenie przekazuje plik o nazwie PlanningData do obiektu BLOB o nazwie Planning2015.</span><span class="sxs-lookup"><span data-stu-id="c509d-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="c509d-113">Przykład 2: przekazywanie wszystkich plików w folderze bieżącym</span><span class="sxs-lookup"><span data-stu-id="c509d-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="c509d-114">To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem do pobierania wszystkich plików w bieżącym folderze i podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="c509d-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c509d-115">Polecenie cmdlet **Set-AzStorageBlobContent** umożliwia przekazanie plików do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="c509d-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="c509d-116">Przykład 3: zastąpienie istniejącego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="c509d-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="c509d-117">To polecenie uzyskuje obiekt BLOB o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzStorageBlob, a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c509d-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="c509d-118">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="c509d-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="c509d-119">To polecenie nie określa parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="c509d-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="c509d-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c509d-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="c509d-121">Jeśli potwierdzisz polecenie, polecenie cmdlet zastąpi istniejący obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="c509d-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="c509d-122">Przykład 4: przekazywanie pliku do kontenera przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="c509d-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="c509d-123">To polecenie uzyskuje kontener, który zaczyna się od ciągu ContosoUpload, przy użyciu polecenia cmdlet **Get-AzStorageContainer** , a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c509d-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="c509d-124">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="c509d-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="c509d-125">Przykład 5: przekazywanie pliku do obiektu BLOB strony za pomocą metadanych i PremiumPageBlobTier jako P10</span><span class="sxs-lookup"><span data-stu-id="c509d-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="c509d-126">Pierwsze polecenie tworzy tabelę skrótów zawierającą metadane dla obiektu BLOB i zapisuje tę tabelę w zmiennej $Metadata.</span><span class="sxs-lookup"><span data-stu-id="c509d-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="c509d-127">Drugie polecenie przekazuje plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="c509d-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="c509d-128">Obiekt BLOB zawiera metadane przechowywane w $Metadata i ma PremiumPageBlobTier jako P10.</span><span class="sxs-lookup"><span data-stu-id="c509d-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="c509d-129">Przykład 6: przekazywanie pliku do obiektu BLOB z określonymi właściwościami obiektu BLOB i Ustawianie StandardBlobTier jako schłodzenia</span><span class="sxs-lookup"><span data-stu-id="c509d-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool
```

<span data-ttu-id="c509d-130">To polecenie wysyła plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads z określonymi właściwościami obiektu BLOB i ustawia StandardBlobTier jako Superpasek.</span><span class="sxs-lookup"><span data-stu-id="c509d-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>

## <span data-ttu-id="c509d-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c509d-131">PARAMETERS</span></span>

### <span data-ttu-id="c509d-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c509d-132">-AsJob</span></span>
<span data-ttu-id="c509d-133">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="c509d-133">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c509d-134">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="c509d-134">-Blob</span></span>
<span data-ttu-id="c509d-135">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c509d-135">Specifies the name of a blob.</span></span>
<span data-ttu-id="c509d-136">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c509d-136">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="c509d-137">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="c509d-137">-BlobType</span></span>
<span data-ttu-id="c509d-138">Określa typ obiektu BLOB, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c509d-138">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="c509d-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c509d-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c509d-140">Drukowany</span><span class="sxs-lookup"><span data-stu-id="c509d-140">Block</span></span>
- <span data-ttu-id="c509d-141">Strona wartość domyślna to Block.</span><span class="sxs-lookup"><span data-stu-id="c509d-141">Page The default value is Block.</span></span>

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

### <span data-ttu-id="c509d-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c509d-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c509d-143">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c509d-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c509d-144">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c509d-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c509d-145">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c509d-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c509d-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c509d-146">-CloudBlob</span></span>
<span data-ttu-id="c509d-147">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="c509d-147">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="c509d-148">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="c509d-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509d-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c509d-149">-CloudBlobContainer</span></span>
<span data-ttu-id="c509d-150">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c509d-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="c509d-151">To polecenie cmdlet umożliwia przekazywanie zawartości do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c509d-151">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="c509d-152">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="c509d-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c509d-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c509d-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c509d-154">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c509d-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c509d-155">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c509d-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c509d-156">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="c509d-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c509d-157">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c509d-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c509d-158">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c509d-158">The default value is 10.</span></span>

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

### <span data-ttu-id="c509d-159">-Kontener</span><span class="sxs-lookup"><span data-stu-id="c509d-159">-Container</span></span>
<span data-ttu-id="c509d-160">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="c509d-160">Specifies the name of a container.</span></span>
<span data-ttu-id="c509d-161">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c509d-161">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="c509d-162">-Context</span><span class="sxs-lookup"><span data-stu-id="c509d-162">-Context</span></span>
<span data-ttu-id="c509d-163">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c509d-163">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c509d-164">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c509d-164">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="c509d-165">Aby użyć kontekstu magazynu utworzonego na podstawie tokenu SAS bez uprawnień do odczytu, należy dodać parametr Add-Force, aby pominąć sprawdzanie obiektu BLOB Check.</span><span class="sxs-lookup"><span data-stu-id="c509d-165">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="c509d-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c509d-166">-DefaultProfile</span></span>
<span data-ttu-id="c509d-167">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c509d-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c509d-168">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="c509d-168">-File</span></span>
<span data-ttu-id="c509d-169">Określa lokalną ścieżkę do pliku, który ma zostać przekazany jako zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c509d-169">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="c509d-170">-Force</span><span class="sxs-lookup"><span data-stu-id="c509d-170">-Force</span></span>
<span data-ttu-id="c509d-171">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c509d-171">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c509d-172">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c509d-172">-Metadata</span></span>
<span data-ttu-id="c509d-173">Określa metadane przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c509d-173">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="c509d-174">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="c509d-174">-PremiumPageBlobTier</span></span>
<span data-ttu-id="c509d-175">Warstwa obiektu BLOB strony</span><span class="sxs-lookup"><span data-stu-id="c509d-175">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c509d-176">-Properties</span><span class="sxs-lookup"><span data-stu-id="c509d-176">-Properties</span></span>
<span data-ttu-id="c509d-177">Określa właściwości przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c509d-177">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="c509d-178">Obsługiwane właściwości to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="c509d-178">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="c509d-179">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c509d-179">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c509d-180">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="c509d-180">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c509d-181">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="c509d-181">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c509d-182">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="c509d-182">-StandardBlobTier</span></span>
<span data-ttu-id="c509d-183">Blokada warstwy obiektu BLOB, prawidłowe wartości to Hot/chłodna/archiwum.</span><span class="sxs-lookup"><span data-stu-id="c509d-183">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="c509d-184">Zobacz szczegóły https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="c509d-184">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="c509d-185">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c509d-185">-Confirm</span></span>
<span data-ttu-id="c509d-186">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c509d-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c509d-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c509d-187">-WhatIf</span></span>
<span data-ttu-id="c509d-188">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c509d-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c509d-189">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c509d-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c509d-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c509d-190">CommonParameters</span></span>
<span data-ttu-id="c509d-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c509d-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c509d-192">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c509d-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c509d-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c509d-193">INPUTS</span></span>

### <span data-ttu-id="c509d-194">System. String</span><span class="sxs-lookup"><span data-stu-id="c509d-194">System.String</span></span>

### <span data-ttu-id="c509d-195">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c509d-195">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="c509d-196">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c509d-196">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c509d-197">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c509d-197">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c509d-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c509d-198">OUTPUTS</span></span>

### <span data-ttu-id="c509d-199">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c509d-199">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c509d-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c509d-200">NOTES</span></span>

## <span data-ttu-id="c509d-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c509d-201">RELATED LINKS</span></span>

[<span data-ttu-id="c509d-202">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c509d-202">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="c509d-203">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c509d-203">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c509d-204">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c509d-204">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
