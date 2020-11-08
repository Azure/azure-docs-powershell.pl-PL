---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: a71995015a8345b3ba181d92ba17e4dd258b169b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224740"
---
# <span data-ttu-id="8a06d-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8a06d-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="8a06d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a06d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a06d-103">Wysyła plik lokalny do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8a06d-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="8a06d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a06d-104">SYNTAX</span></span>

### <span data-ttu-id="8a06d-105">SendManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a06d-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a06d-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="8a06d-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a06d-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="8a06d-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a06d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8a06d-108">DESCRIPTION</span></span>
<span data-ttu-id="8a06d-109">Polecenie cmdlet **Set-AzStorageBlobContent** umożliwia przekazywanie pliku lokalnego do obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8a06d-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="8a06d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a06d-110">EXAMPLES</span></span>

### <span data-ttu-id="8a06d-111">Przykład 1: przekazywanie nazwanego pliku</span><span class="sxs-lookup"><span data-stu-id="8a06d-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="8a06d-112">To polecenie przekazuje plik o nazwie PlanningData do obiektu BLOB o nazwie Planning2015.</span><span class="sxs-lookup"><span data-stu-id="8a06d-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="8a06d-113">Przykład 2: przekazywanie wszystkich plików w folderze bieżącym</span><span class="sxs-lookup"><span data-stu-id="8a06d-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="8a06d-114">To polecenie używa podstawowego polecenia cmdlet programu Windows PowerShell Get-ChildItem do pobierania wszystkich plików w bieżącym folderze i podfolderach, a następnie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8a06d-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8a06d-115">Polecenie cmdlet **Set-AzStorageBlobContent** umożliwia przekazanie plików do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="8a06d-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="8a06d-116">Przykład 3: zastąpienie istniejącego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="8a06d-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="8a06d-117">To polecenie uzyskuje obiekt BLOB o nazwie Planning2015 w kontenerze ContosoUploads przy użyciu polecenia cmdlet Get-AzStorageBlob, a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a06d-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="8a06d-118">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="8a06d-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="8a06d-119">To polecenie nie określa parametru *Force* .</span><span class="sxs-lookup"><span data-stu-id="8a06d-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="8a06d-120">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8a06d-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="8a06d-121">Jeśli potwierdzisz polecenie, polecenie cmdlet zastąpi istniejący obiekt BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a06d-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="8a06d-122">Przykład 4: przekazywanie pliku do kontenera przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="8a06d-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="8a06d-123">To polecenie uzyskuje kontener, który zaczyna się od ciągu ContosoUpload, przy użyciu polecenia cmdlet **Get-AzStorageContainer** , a następnie przekazuje ten obiekt BLOB do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a06d-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="8a06d-124">Polecenie przekazuje plik o nazwie ContosoPlanning jako Planning2015.</span><span class="sxs-lookup"><span data-stu-id="8a06d-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="8a06d-125">Przykład 5: przekazywanie pliku do obiektu BLOB strony za pomocą metadanych i PremiumPageBlobTier jako P10</span><span class="sxs-lookup"><span data-stu-id="8a06d-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="8a06d-126">Pierwsze polecenie tworzy tabelę skrótów zawierającą metadane dla obiektu BLOB i zapisuje tę tabelę w zmiennej $Metadata.</span><span class="sxs-lookup"><span data-stu-id="8a06d-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="8a06d-127">Drugie polecenie przekazuje plik o nazwie ContosoPlanning do kontenera o nazwie ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="8a06d-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="8a06d-128">Obiekt BLOB zawiera metadane przechowywane w $Metadata i ma PremiumPageBlobTier jako P10.</span><span class="sxs-lookup"><span data-stu-id="8a06d-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="8a06d-129">Przykład 6: przekazywanie pliku do obiektu BLOB z określonymi właściwościami obiektu BLOB i Ustawianie StandardBlobTier jako schłodzenia</span><span class="sxs-lookup"><span data-stu-id="8a06d-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="8a06d-130">To polecenie umożliwia przekazywanie pliku c:\temp\index.html do kontenera o nazwie contosouploads z określonymi właściwościami obiektu BLOB i Ustawianie StandardBlobTier jako schłodzenia.</span><span class="sxs-lookup"><span data-stu-id="8a06d-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="8a06d-131">To polecenie pobiera wartość ContentType ustawiona na właściwości obiektu BLOB za pośrednictwem interfejsu API [System. Web. MimeMapping]:: GetMimeMapping ().</span><span class="sxs-lookup"><span data-stu-id="8a06d-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

## <span data-ttu-id="8a06d-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a06d-132">PARAMETERS</span></span>

### <span data-ttu-id="8a06d-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a06d-133">-AsJob</span></span>
<span data-ttu-id="8a06d-134">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="8a06d-134">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8a06d-135">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="8a06d-135">-Blob</span></span>
<span data-ttu-id="8a06d-136">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a06d-136">Specifies the name of a blob.</span></span>
<span data-ttu-id="8a06d-137">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8a06d-137">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="8a06d-138">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="8a06d-138">-BlobType</span></span>
<span data-ttu-id="8a06d-139">Określa typ obiektu BLOB, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a06d-139">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="8a06d-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8a06d-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8a06d-141">Drukowany</span><span class="sxs-lookup"><span data-stu-id="8a06d-141">Block</span></span>
- <span data-ttu-id="8a06d-142">Strona wartość domyślna to Block.</span><span class="sxs-lookup"><span data-stu-id="8a06d-142">Page The default value is Block.</span></span>

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

### <span data-ttu-id="8a06d-143">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a06d-143">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8a06d-144">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="8a06d-144">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8a06d-145">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="8a06d-145">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8a06d-146">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="8a06d-146">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8a06d-147">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8a06d-147">-CloudBlob</span></span>
<span data-ttu-id="8a06d-148">Określa obiekt **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="8a06d-148">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="8a06d-149">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="8a06d-149">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="8a06d-150">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8a06d-150">-CloudBlobContainer</span></span>
<span data-ttu-id="8a06d-151">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8a06d-151">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="8a06d-152">To polecenie cmdlet umożliwia przekazywanie zawartości do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8a06d-152">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="8a06d-153">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="8a06d-153">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="8a06d-154">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8a06d-154">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8a06d-155">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8a06d-155">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8a06d-156">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8a06d-156">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8a06d-157">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="8a06d-157">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8a06d-158">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="8a06d-158">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8a06d-159">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8a06d-159">The default value is 10.</span></span>

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

### <span data-ttu-id="8a06d-160">-Kontener</span><span class="sxs-lookup"><span data-stu-id="8a06d-160">-Container</span></span>
<span data-ttu-id="8a06d-161">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="8a06d-161">Specifies the name of a container.</span></span>
<span data-ttu-id="8a06d-162">To polecenie cmdlet umożliwia przekazywanie pliku do obiektu BLOB w kontenerze, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8a06d-162">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="8a06d-163">-Context</span><span class="sxs-lookup"><span data-stu-id="8a06d-163">-Context</span></span>
<span data-ttu-id="8a06d-164">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8a06d-164">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8a06d-165">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8a06d-165">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="8a06d-166">Aby użyć kontekstu magazynu utworzonego na podstawie tokenu SAS bez uprawnień do odczytu, należy dodać parametr Add-Force, aby pominąć sprawdzanie obiektu BLOB Check.</span><span class="sxs-lookup"><span data-stu-id="8a06d-166">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="8a06d-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a06d-167">-DefaultProfile</span></span>
<span data-ttu-id="8a06d-168">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a06d-168">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a06d-169">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="8a06d-169">-File</span></span>
<span data-ttu-id="8a06d-170">Określa lokalną ścieżkę do pliku, który ma zostać przekazany jako zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a06d-170">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="8a06d-171">-Force</span><span class="sxs-lookup"><span data-stu-id="8a06d-171">-Force</span></span>
<span data-ttu-id="8a06d-172">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8a06d-172">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8a06d-173">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8a06d-173">-Metadata</span></span>
<span data-ttu-id="8a06d-174">Określa metadane przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a06d-174">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="8a06d-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="8a06d-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="8a06d-176">Warstwa obiektu BLOB strony</span><span class="sxs-lookup"><span data-stu-id="8a06d-176">Page Blob Tier</span></span>

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

### <span data-ttu-id="8a06d-177">-Properties</span><span class="sxs-lookup"><span data-stu-id="8a06d-177">-Properties</span></span>
<span data-ttu-id="8a06d-178">Określa właściwości przekazanego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a06d-178">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="8a06d-179">Obsługiwane właściwości to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="8a06d-179">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="8a06d-180">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a06d-180">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8a06d-181">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="8a06d-181">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8a06d-182">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="8a06d-182">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8a06d-183">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="8a06d-183">-StandardBlobTier</span></span>
<span data-ttu-id="8a06d-184">Blokada warstwy obiektu BLOB, prawidłowe wartości to Hot/chłodna/archiwum.</span><span class="sxs-lookup"><span data-stu-id="8a06d-184">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="8a06d-185">Zobacz szczegóły https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="8a06d-185">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="8a06d-186">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a06d-186">-Confirm</span></span>
<span data-ttu-id="8a06d-187">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a06d-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a06d-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a06d-188">-WhatIf</span></span>
<span data-ttu-id="8a06d-189">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a06d-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a06d-190">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a06d-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a06d-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a06d-191">CommonParameters</span></span>
<span data-ttu-id="8a06d-192">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a06d-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a06d-193">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a06d-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a06d-194">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a06d-194">INPUTS</span></span>

### <span data-ttu-id="8a06d-195">System. String</span><span class="sxs-lookup"><span data-stu-id="8a06d-195">System.String</span></span>

### <span data-ttu-id="8a06d-196">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8a06d-196">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="8a06d-197">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8a06d-197">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="8a06d-198">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8a06d-198">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8a06d-199">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a06d-199">OUTPUTS</span></span>

### <span data-ttu-id="8a06d-200">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8a06d-200">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="8a06d-201">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a06d-201">NOTES</span></span>

## <span data-ttu-id="8a06d-202">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a06d-202">RELATED LINKS</span></span>

[<span data-ttu-id="8a06d-203">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8a06d-203">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="8a06d-204">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8a06d-204">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="8a06d-205">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8a06d-205">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
