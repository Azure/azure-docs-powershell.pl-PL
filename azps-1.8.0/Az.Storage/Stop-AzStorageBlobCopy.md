---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: e644d1d4813aeea30624576a3b4f1d3fb2cbc672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707486"
---
# <span data-ttu-id="06bc8-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="06bc8-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="06bc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="06bc8-103">Zatrzymuje operację kopiowania.</span><span class="sxs-lookup"><span data-stu-id="06bc8-103">Stops a copy operation.</span></span>

## <span data-ttu-id="06bc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06bc8-104">SYNTAX</span></span>

### <span data-ttu-id="06bc8-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06bc8-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06bc8-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="06bc8-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06bc8-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="06bc8-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06bc8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="06bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="06bc8-109">Polecenie cmdlet **stop-AzStorageBlobCopy** zatrzymuje operację kopiowania do określonego docelowego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="06bc8-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="06bc8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="06bc8-111">Przykład 1: zatrzymywanie operacji kopiowania według nazwy</span><span class="sxs-lookup"><span data-stu-id="06bc8-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="06bc8-112">To polecenie zatrzymuje operację kopiowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="06bc8-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="06bc8-113">Przykład 2: zatrzymywanie operacji kopiowania za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="06bc8-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="06bc8-114">To polecenie zatrzymuje operację kopiowania, przesyłając kontener w rurociągu, korzystając z polecenia **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="06bc8-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="06bc8-115">Przykład 3: zatrzymywanie operacji kopiowania za pomocą potoku i Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="06bc8-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="06bc8-116">W tym przykładzie zatrzymano operację kopiowania, przesyłając kontener w potoku za pomocą polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="06bc8-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="06bc8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06bc8-117">PARAMETERS</span></span>

### <span data-ttu-id="06bc8-118">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="06bc8-118">-Blob</span></span>
<span data-ttu-id="06bc8-119">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="06bc8-119">Specifies the name of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bc8-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06bc8-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="06bc8-121">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="06bc8-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="06bc8-122">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="06bc8-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="06bc8-123">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="06bc8-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="06bc8-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="06bc8-124">-CloudBlob</span></span>
<span data-ttu-id="06bc8-125">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06bc8-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="06bc8-126">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="06bc8-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="06bc8-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="06bc8-127">-CloudBlobContainer</span></span>
<span data-ttu-id="06bc8-128">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06bc8-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="06bc8-129">Możesz utworzyć obiekt lub użyć Get-AzStorageContainer polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bc8-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="06bc8-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="06bc8-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="06bc8-131">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="06bc8-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="06bc8-132">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="06bc8-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="06bc8-133">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="06bc8-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="06bc8-134">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="06bc8-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="06bc8-135">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="06bc8-135">The default value is 10.</span></span>

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

### <span data-ttu-id="06bc8-136">-Kontener</span><span class="sxs-lookup"><span data-stu-id="06bc8-136">-Container</span></span>
<span data-ttu-id="06bc8-137">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="06bc8-137">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bc8-138">-Context</span><span class="sxs-lookup"><span data-stu-id="06bc8-138">-Context</span></span>
<span data-ttu-id="06bc8-139">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="06bc8-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="06bc8-140">Kontekst można utworzyć przy użyciu polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="06bc8-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="06bc8-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="06bc8-141">-CopyId</span></span>
<span data-ttu-id="06bc8-142">Określa identyfikator kopii.</span><span class="sxs-lookup"><span data-stu-id="06bc8-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="06bc8-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06bc8-143">-DefaultProfile</span></span>
<span data-ttu-id="06bc8-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06bc8-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06bc8-145">-Force</span><span class="sxs-lookup"><span data-stu-id="06bc8-145">-Force</span></span>
<span data-ttu-id="06bc8-146">Zatrzymuje bieżące zadanie kopiowania na określonym obiekcie blob bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06bc8-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="06bc8-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06bc8-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="06bc8-148">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="06bc8-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="06bc8-149">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="06bc8-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="06bc8-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06bc8-150">-Confirm</span></span>
<span data-ttu-id="06bc8-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bc8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06bc8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06bc8-152">-WhatIf</span></span>
<span data-ttu-id="06bc8-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06bc8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06bc8-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06bc8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06bc8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bc8-155">CommonParameters</span></span>
<span data-ttu-id="06bc8-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06bc8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06bc8-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06bc8-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bc8-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06bc8-158">INPUTS</span></span>

### <span data-ttu-id="06bc8-159">Microsoft. platformy windowsazure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="06bc8-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="06bc8-160">Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="06bc8-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="06bc8-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06bc8-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="06bc8-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06bc8-162">OUTPUTS</span></span>

### <span data-ttu-id="06bc8-163">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="06bc8-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="06bc8-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06bc8-164">NOTES</span></span>

## <span data-ttu-id="06bc8-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06bc8-165">RELATED LINKS</span></span>

[<span data-ttu-id="06bc8-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="06bc8-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="06bc8-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="06bc8-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="06bc8-168">Start — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="06bc8-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="06bc8-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="06bc8-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
