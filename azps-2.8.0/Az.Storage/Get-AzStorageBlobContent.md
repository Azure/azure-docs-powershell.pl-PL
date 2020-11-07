---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 320de9e1dab757265d626b1df34e5049c691b7bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887733"
---
# <span data-ttu-id="bbfcb-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bbfcb-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="bbfcb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbfcb-102">SYNOPSIS</span></span>
<span data-ttu-id="bbfcb-103">Pobiera obiekt blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="bbfcb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbfcb-104">SYNTAX</span></span>

### <span data-ttu-id="bbfcb-105">ReceiveManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bbfcb-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbfcb-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="bbfcb-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbfcb-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="bbfcb-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbfcb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bbfcb-108">DESCRIPTION</span></span>
<span data-ttu-id="bbfcb-109">Polecenie cmdlet **Get-AzStorageBlobContent** umożliwia pobranie określonego obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="bbfcb-110">Jeśli nazwa obiektu BLOB nie jest prawidłowa na komputerze lokalnym, to polecenie cmdlet automatycznie rozpoznaje je, jeśli to możliwe.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="bbfcb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbfcb-111">EXAMPLES</span></span>

### <span data-ttu-id="bbfcb-112">Przykład 1: pobieranie zawartości obiektu BLOB według nazwy</span><span class="sxs-lookup"><span data-stu-id="bbfcb-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="bbfcb-113">To polecenie umożliwia pobranie obiektu BLOB według nazwy.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="bbfcb-114">Przykład 2: pobieranie zawartości obiektu BLOB za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="bbfcb-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="bbfcb-115">To polecenie używa potoku do znajdowania i pobierania zawartości obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="bbfcb-116">Przykład 3: pobieranie zawartości obiektu BLOB za pomocą potoku i znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="bbfcb-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="bbfcb-117">W tym przykładzie użyto symbolu wieloznacznego gwiazdki i rurociągu do znajdowania i pobierania zawartości obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="bbfcb-118">Przykład 4: pobranie obiektu BLOB i zapisanie go w zmiennej, a następnie pobranie zawartości obiektu BLOB za pomocą obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="bbfcb-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="bbfcb-119">W tym przykładzie najpierw uzyskujesz obiekt BLOB i zapisujesz go w zmiennej, a następnie pobierasz zawartość obiektu BLOB za pomocą obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="bbfcb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbfcb-120">PARAMETERS</span></span>

### <span data-ttu-id="bbfcb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbfcb-121">-AsJob</span></span>
<span data-ttu-id="bbfcb-122">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bbfcb-123">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="bbfcb-123">-Blob</span></span>
<span data-ttu-id="bbfcb-124">Określa nazwę obiektu BLOB, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-124">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="bbfcb-125">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="bbfcb-125">-CheckMd5</span></span>
<span data-ttu-id="bbfcb-126">Określa, czy ma być sprawdzana suma Md5 dla pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-126">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="bbfcb-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbfcb-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bbfcb-128">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bbfcb-129">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bbfcb-130">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bbfcb-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bbfcb-131">-CloudBlob</span></span>
<span data-ttu-id="bbfcb-132">Określa obiekt BLOB chmury.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-132">Specifies a cloud blob.</span></span>
<span data-ttu-id="bbfcb-133">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="bbfcb-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bbfcb-134">-CloudBlobContainer</span></span>
<span data-ttu-id="bbfcb-135">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-135">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="bbfcb-136">Możesz je utworzyć lub użyć Get-AzStorageContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-136">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="bbfcb-137">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bbfcb-137">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bbfcb-138">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-138">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bbfcb-139">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-139">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bbfcb-140">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-140">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bbfcb-141">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-141">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bbfcb-142">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-142">The default value is 10.</span></span>

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

### <span data-ttu-id="bbfcb-143">-Kontener</span><span class="sxs-lookup"><span data-stu-id="bbfcb-143">-Container</span></span>
<span data-ttu-id="bbfcb-144">Określa nazwę kontenera zawierającego obiekt BLOB, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-144">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="bbfcb-145">-Context</span><span class="sxs-lookup"><span data-stu-id="bbfcb-145">-Context</span></span>
<span data-ttu-id="bbfcb-146">Określa konto usługi Azure Storage, z którego chcesz pobrać zawartość obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-146">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="bbfcb-147">Aby utworzyć kontekst miejsca do magazynowania, możesz użyć polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-147">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="bbfcb-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfcb-148">-DefaultProfile</span></span>
<span data-ttu-id="bbfcb-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbfcb-150">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="bbfcb-150">-Destination</span></span>
<span data-ttu-id="bbfcb-151">Określa lokalizację, w której ma zostać zapisany pobrany plik.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-151">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="bbfcb-152">-Force</span><span class="sxs-lookup"><span data-stu-id="bbfcb-152">-Force</span></span>
<span data-ttu-id="bbfcb-153">Zastępuje istniejący plik bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-153">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="bbfcb-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbfcb-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bbfcb-155">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="bbfcb-156">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="bbfcb-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbfcb-157">-Confirm</span></span>
<span data-ttu-id="bbfcb-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbfcb-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbfcb-159">-WhatIf</span></span>
<span data-ttu-id="bbfcb-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbfcb-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbfcb-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbfcb-162">CommonParameters</span></span>
<span data-ttu-id="bbfcb-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbfcb-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbfcb-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbfcb-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbfcb-165">INPUTS</span></span>

### <span data-ttu-id="bbfcb-166">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bbfcb-166">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="bbfcb-167">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bbfcb-167">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="bbfcb-168">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbfcb-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bbfcb-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbfcb-169">OUTPUTS</span></span>

### <span data-ttu-id="bbfcb-170">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bbfcb-170">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="bbfcb-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbfcb-171">NOTES</span></span>
* <span data-ttu-id="bbfcb-172">Jeśli nazwa obiektu BLOB jest nieprawidłowa dla komputera lokalnego, to polecenie cmdlet automatycznie rozpoznaje je, jeśli jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="bbfcb-172">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="bbfcb-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbfcb-173">RELATED LINKS</span></span>

[<span data-ttu-id="bbfcb-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bbfcb-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="bbfcb-175">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bbfcb-175">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="bbfcb-176">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bbfcb-176">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
