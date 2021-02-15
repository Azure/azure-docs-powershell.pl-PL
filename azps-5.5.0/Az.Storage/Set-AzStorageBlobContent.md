---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 388adccb9578c695055815ab6e6de5478958621f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183155"
---
# <span data-ttu-id="743df-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="743df-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="743df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="743df-102">SYNOPSIS</span></span>
<span data-ttu-id="743df-103">Przekazanie pliku lokalnego do obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="743df-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="743df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="743df-104">SYNTAX</span></span>

### <span data-ttu-id="743df-105">SendManual (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="743df-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="743df-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="743df-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="743df-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="743df-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="743df-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="743df-108">DESCRIPTION</span></span>
<span data-ttu-id="743df-109">Polecenie **cmdlet Set-AzStorageBlobContent** przekaże plik lokalny do obiektu blob usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="743df-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="743df-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="743df-110">EXAMPLES</span></span>

### <span data-ttu-id="743df-111">Przykład 1. Przekazywanie nazwanego pliku</span><span class="sxs-lookup"><span data-stu-id="743df-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="743df-112">To polecenie przekaże plik o nazwie PlanningData do obiektu blob o nazwie Planning2015.</span><span class="sxs-lookup"><span data-stu-id="743df-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="743df-113">Przykład 2. Przekazywanie wszystkich plików w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="743df-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="743df-114">To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem w celu uzyskania wszystkich plików w bieżącym folderze i w podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="743df-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="743df-115">Polecenie **cmdlet Set-AzStorageBlobContent** przekaże pliki do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="743df-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="743df-116">Przykład 3. Zastępowanie istniejącego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="743df-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="743df-117">To polecenie pobiera obiekt blob o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzStorageBlob, Get-AzStorageBlob następnie przekazuje ten obiekt blob do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743df-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="743df-118">Polecenie przekaże plik o nazwie ContosoPlanning jako Planowanie2015.</span><span class="sxs-lookup"><span data-stu-id="743df-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="743df-119">To polecenie nie określa *parametru Force.*</span><span class="sxs-lookup"><span data-stu-id="743df-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="743df-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="743df-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="743df-121">Jeśli potwierdzisz to polecenie, polecenie cmdlet zastąpi istniejący obiekt blob.</span><span class="sxs-lookup"><span data-stu-id="743df-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="743df-122">Przykład 4. Przekazanie pliku do kontenera przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="743df-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="743df-123">To polecenie pobiera kontener, który zaczyna się ciągiem ContosoUpload, za pomocą polecenia cmdlet **Get-AzStorageContainer,** a następnie przekazuje ten obiekt blob do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743df-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="743df-124">Polecenie przekaże plik o nazwie ContosoPlanning jako Planowanie2015.</span><span class="sxs-lookup"><span data-stu-id="743df-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="743df-125">Przykład 5. Przekazywanie pliku do obiektu blob strony z metadanymi i właściwością PremiumPageBlobTier jako P10</span><span class="sxs-lookup"><span data-stu-id="743df-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="743df-126">Pierwsze polecenie tworzy tabelę skrótu zawierającą metadane dla obiektu blob i przechowuje tabelę tego skrótu w $Metadata tabeli.</span><span class="sxs-lookup"><span data-stu-id="743df-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="743df-127">Drugie polecenie przekaże plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="743df-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="743df-128">Obiekt blob zawiera metadane przechowywane w u $Metadata i ma stronę PremiumPageBlobTier jako P10.</span><span class="sxs-lookup"><span data-stu-id="743df-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="743df-129">Przykład 6. Przekazanie pliku do obiektu blob z określonymi właściwościami obiektu blob i ustawienie standardowegoBlobTier jako cool</span><span class="sxs-lookup"><span data-stu-id="743df-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="743df-130">To polecenie przekaże plik c:\temp\index.html do kontenera o nazwie contosouploads z określonymi właściwościami obiektów blob i ustaw standardBlobTier jako cool.</span><span class="sxs-lookup"><span data-stu-id="743df-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="743df-131">To polecenie pobiera wartość ContentType ustawioną na właściwości obiektów blob przez interfejs API [System.Web.MimeMapping]::GetMimeMapping().</span><span class="sxs-lookup"><span data-stu-id="743df-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="743df-132">Przykład 7. Przekazywanie pliku do obiektu blob z zakresem szyfrowania</span><span class="sxs-lookup"><span data-stu-id="743df-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="743df-133">To polecenie przekaże plik do obiektu blob z zakresem szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="743df-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="743df-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="743df-134">PARAMETERS</span></span>

### <span data-ttu-id="743df-135">— AsJob</span><span class="sxs-lookup"><span data-stu-id="743df-135">-AsJob</span></span>
<span data-ttu-id="743df-136">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="743df-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="743df-137">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="743df-137">-Blob</span></span>
<span data-ttu-id="743df-138">Określa nazwę obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="743df-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="743df-139">To polecenie cmdlet przekaże plik do obiektu blob magazynu platformy Azure, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="743df-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="743df-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="743df-140">-BlobType</span></span>
<span data-ttu-id="743df-141">Określa typ obiektu blob, który jest przesyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743df-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="743df-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="743df-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="743df-143">Zablokuj</span><span class="sxs-lookup"><span data-stu-id="743df-143">Block</span></span>
- <span data-ttu-id="743df-144">Strona</span><span class="sxs-lookup"><span data-stu-id="743df-144">Page</span></span>
- <span data-ttu-id="743df-145">Dołącz Wartość domyślna to Block (Blokuj).</span><span class="sxs-lookup"><span data-stu-id="743df-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="743df-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="743df-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="743df-147">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="743df-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="743df-148">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="743df-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="743df-149">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="743df-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="743df-150">— CloudBlob</span><span class="sxs-lookup"><span data-stu-id="743df-150">-CloudBlob</span></span>
<span data-ttu-id="743df-151">Określa obiekt **CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="743df-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="743df-152">Aby uzyskać obiekt **CloudBlob,** użyj Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743df-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="743df-153">- CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="743df-153">-CloudBlobContainer</span></span>
<span data-ttu-id="743df-154">Określa obiekt **CloudBlobContainer** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="743df-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="743df-155">To polecenie cmdlet przekaże zawartość do obiektu blob w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="743df-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="743df-156">Aby uzyskać obiekt **CloudBlobContainer,** użyj Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743df-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="743df-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="743df-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="743df-158">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="743df-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="743df-159">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="743df-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="743df-160">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="743df-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="743df-161">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="743df-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="743df-162">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="743df-162">The default value is 10.</span></span>

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

### <span data-ttu-id="743df-163">— Kontener</span><span class="sxs-lookup"><span data-stu-id="743df-163">-Container</span></span>
<span data-ttu-id="743df-164">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="743df-164">Specifies the name of a container.</span></span>
<span data-ttu-id="743df-165">To polecenie cmdlet przekaże plik do obiektu blob w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="743df-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="743df-166">— kontekst</span><span class="sxs-lookup"><span data-stu-id="743df-166">-Context</span></span>
<span data-ttu-id="743df-167">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="743df-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="743df-168">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743df-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="743df-169">Aby użyć kontekstu magazynu utworzonego na podstawie tokenu SAS bez uprawnienia do odczytu, musisz dodać parametr -Force, aby pominąć sprawdzanie istnienia obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="743df-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="743df-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743df-170">-DefaultProfile</span></span>
<span data-ttu-id="743df-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="743df-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="743df-172">- EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="743df-172">-EncryptionScope</span></span>
<span data-ttu-id="743df-173">Zakres szyfrowania, który ma być używany podczas żądania do obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="743df-173">Encryption scope to be used when making requests to the blob.</span></span>

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

### <span data-ttu-id="743df-174">— Plik</span><span class="sxs-lookup"><span data-stu-id="743df-174">-File</span></span>
<span data-ttu-id="743df-175">Określa lokalną ścieżkę pliku do przekazania jako zawartość obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="743df-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="743df-176">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="743df-176">-Force</span></span>
<span data-ttu-id="743df-177">Wskazuje, że to polecenie cmdlet zastępuje istniejący obiekt blob bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="743df-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="743df-178">— Metadane</span><span class="sxs-lookup"><span data-stu-id="743df-178">-Metadata</span></span>
<span data-ttu-id="743df-179">Określa metadane dla przekazanego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="743df-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="743df-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="743df-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="743df-181">Warstwa obiektów blob strony</span><span class="sxs-lookup"><span data-stu-id="743df-181">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743df-182">— Properties</span><span class="sxs-lookup"><span data-stu-id="743df-182">-Properties</span></span>
<span data-ttu-id="743df-183">Określa właściwości przekazanego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="743df-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="743df-184">Obsługiwane właściwości to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="743df-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="743df-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="743df-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="743df-186">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="743df-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="743df-187">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="743df-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="743df-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="743df-188">-StandardBlobTier</span></span>
<span data-ttu-id="743df-189">Blokuj warstwę obiektów blob, prawidłowe wartości to Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="743df-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="743df-190">Zobacz szczegóły w https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="743df-190">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="743df-191">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="743df-191">-Confirm</span></span>
<span data-ttu-id="743df-192">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="743df-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="743df-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="743df-193">-WhatIf</span></span>
<span data-ttu-id="743df-194">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743df-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="743df-195">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="743df-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="743df-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743df-196">CommonParameters</span></span>
<span data-ttu-id="743df-197">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743df-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743df-198">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743df-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743df-199">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="743df-199">INPUTS</span></span>

### <span data-ttu-id="743df-200">System.String</span><span class="sxs-lookup"><span data-stu-id="743df-200">System.String</span></span>

### <span data-ttu-id="743df-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="743df-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="743df-202">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="743df-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="743df-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="743df-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="743df-204">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="743df-204">OUTPUTS</span></span>

### <span data-ttu-id="743df-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="743df-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="743df-206">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="743df-206">NOTES</span></span>

## <span data-ttu-id="743df-207">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="743df-207">RELATED LINKS</span></span>

[<span data-ttu-id="743df-208">Get-AzstorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="743df-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="743df-209">Get-AzstorageBlob</span><span class="sxs-lookup"><span data-stu-id="743df-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="743df-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="743df-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
