---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197570"
---
# <span data-ttu-id="b090a-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b090a-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="b090a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b090a-102">SYNOPSIS</span></span>
<span data-ttu-id="b090a-103">Pobiera obiekt blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="b090a-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="b090a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b090a-104">SYNTAX</span></span>

### <span data-ttu-id="b090a-105">ReceiveManual (Default)</span><span class="sxs-lookup"><span data-stu-id="b090a-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b090a-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b090a-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b090a-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b090a-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b090a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b090a-108">DESCRIPTION</span></span>
<span data-ttu-id="b090a-109">Polecenie **cmdlet Get-AzStorageBlobContent** pobiera określony obiekt blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="b090a-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="b090a-110">Jeśli nazwa obiektu blob nie jest prawidłowa dla komputera lokalnego, to polecenie cmdlet automatycznie rozwiązuje ją, jeśli jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="b090a-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="b090a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b090a-111">EXAMPLES</span></span>

### <span data-ttu-id="b090a-112">Przykład 1. Pobieranie zawartości obiektów blob według nazwy</span><span class="sxs-lookup"><span data-stu-id="b090a-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="b090a-113">To polecenie pobiera obiekt blob według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b090a-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="b090a-114">Przykład 2. Pobieranie zawartości obiektów blob przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="b090a-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="b090a-115">To polecenie używa potoku do odnalezienia i pobrania zawartości obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="b090a-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="b090a-116">Przykład 3. Pobieranie zawartości obiektów blob przy użyciu potoku i symbolu wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="b090a-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="b090a-117">W tym przykładzie do znalezienia i pobrania zawartości obiektów blob jest używany symbol wieloznaczny gwiazdki i potok.</span><span class="sxs-lookup"><span data-stu-id="b090a-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="b090a-118">Przykład 4. Pobieranie obiektu blob i zapisywanie go w zmiennej, a następnie pobieranie zawartości obiektów blob z obiektem blob</span><span class="sxs-lookup"><span data-stu-id="b090a-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="b090a-119">W tym przykładzie najpierw pobierz obiekt blob i zapisz go w zmiennej, a następnie pobierz zawartość obiektu blob wraz z tym obiektem blob.</span><span class="sxs-lookup"><span data-stu-id="b090a-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="b090a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b090a-120">PARAMETERS</span></span>

### <span data-ttu-id="b090a-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b090a-121">-AsJob</span></span>
<span data-ttu-id="b090a-122">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="b090a-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b090a-123">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="b090a-123">-Blob</span></span>
<span data-ttu-id="b090a-124">Określa nazwę obiektu blob do pobrania.</span><span class="sxs-lookup"><span data-stu-id="b090a-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b090a-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="b090a-125">-BlobBaseClient</span></span>
<span data-ttu-id="b090a-126">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="b090a-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b090a-127">— CheckMd5</span><span class="sxs-lookup"><span data-stu-id="b090a-127">-CheckMd5</span></span>
<span data-ttu-id="b090a-128">Określa, czy należy sprawdzić sumę Md5 dla pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="b090a-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="b090a-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b090a-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b090a-130">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b090a-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b090a-131">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="b090a-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b090a-132">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="b090a-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b090a-133">— CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b090a-133">-CloudBlob</span></span>
<span data-ttu-id="b090a-134">Określa obiekt blob chmury.</span><span class="sxs-lookup"><span data-stu-id="b090a-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="b090a-135">Aby uzyskać obiekt **CloudBlob,** użyj Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b090a-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b090a-136">- CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b090a-136">-CloudBlobContainer</span></span>
<span data-ttu-id="b090a-137">Określa obiekt **CloudBlobContainer** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b090a-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="b090a-138">Możesz go utworzyć lub użyć Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b090a-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b090a-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b090a-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b090a-140">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b090a-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b090a-141">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b090a-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b090a-142">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="b090a-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b090a-143">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b090a-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b090a-144">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b090a-144">The default value is 10.</span></span>

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

### <span data-ttu-id="b090a-145">— Kontener</span><span class="sxs-lookup"><span data-stu-id="b090a-145">-Container</span></span>
<span data-ttu-id="b090a-146">Określa nazwę kontenera, który zawiera obiekt blob, który chcesz pobrać.</span><span class="sxs-lookup"><span data-stu-id="b090a-146">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b090a-147">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b090a-147">-Context</span></span>
<span data-ttu-id="b090a-148">Określa konto magazynu platformy Azure, z którego chcesz pobrać zawartość obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="b090a-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="b090a-149">Możesz użyć polecenia cmdlet New-AzStorageContext, aby utworzyć kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="b090a-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="b090a-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b090a-150">-DefaultProfile</span></span>
<span data-ttu-id="b090a-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b090a-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b090a-152">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="b090a-152">-Destination</span></span>
<span data-ttu-id="b090a-153">Określa lokalizację przechowywania pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="b090a-153">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b090a-154">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b090a-154">-Force</span></span>
<span data-ttu-id="b090a-155">Zastępuje istniejący plik bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="b090a-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="b090a-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b090a-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b090a-157">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="b090a-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b090a-158">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="b090a-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b090a-159">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b090a-159">-Confirm</span></span>
<span data-ttu-id="b090a-160">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b090a-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b090a-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b090a-161">-WhatIf</span></span>
<span data-ttu-id="b090a-162">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b090a-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b090a-163">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b090a-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b090a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b090a-164">CommonParameters</span></span>
<span data-ttu-id="b090a-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b090a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b090a-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b090a-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b090a-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b090a-167">INPUTS</span></span>

### <span data-ttu-id="b090a-168">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b090a-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b090a-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b090a-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b090a-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b090a-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b090a-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b090a-171">OUTPUTS</span></span>

### <span data-ttu-id="b090a-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b090a-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b090a-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b090a-173">NOTES</span></span>
* <span data-ttu-id="b090a-174">Jeśli nazwa obiektu blob jest nieprawidłowa dla komputera lokalnego, to polecenie cmdlet automatycznie ją rozpozna, jeśli jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="b090a-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="b090a-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b090a-175">RELATED LINKS</span></span>

[<span data-ttu-id="b090a-176">Set-AzstorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b090a-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="b090a-177">Get-AzstorageBlob</span><span class="sxs-lookup"><span data-stu-id="b090a-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="b090a-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b090a-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
