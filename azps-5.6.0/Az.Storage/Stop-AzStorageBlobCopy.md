---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 1be012a9a9c5a62cbd08451849f8d50e9a5d52a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960065"
---
# <span data-ttu-id="0a453-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a453-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="0a453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a453-102">SYNOPSIS</span></span>
<span data-ttu-id="0a453-103">Zatrzymuje operację kopiowania.</span><span class="sxs-lookup"><span data-stu-id="0a453-103">Stops a copy operation.</span></span>

## <span data-ttu-id="0a453-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0a453-104">SYNTAX</span></span>

### <span data-ttu-id="0a453-105">NamePipeline (Default)</span><span class="sxs-lookup"><span data-stu-id="0a453-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a453-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="0a453-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a453-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="0a453-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a453-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0a453-108">DESCRIPTION</span></span>
<span data-ttu-id="0a453-109">Polecenie **cmdlet Stop-AzStorageBlobCopy** zatrzymuje operację kopiowania do określonego obiektu blob miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="0a453-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="0a453-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0a453-110">EXAMPLES</span></span>

### <span data-ttu-id="0a453-111">Przykład 1. Zatrzymywanie kopiowania według nazwy</span><span class="sxs-lookup"><span data-stu-id="0a453-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="0a453-112">To polecenie zatrzymuje operację kopiowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0a453-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="0a453-113">Przykład 2. Zatrzymywanie kopiowania przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="0a453-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="0a453-114">To polecenie zatrzymuje operację kopiowania, przekazując kontener w potoku z **get-azstorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="0a453-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="0a453-115">Przykład 3. Zatrzymywanie kopiowania przy użyciu potoku i Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0a453-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="0a453-116">W tym przykładzie zatrzymano operację kopiowania, przekazując kontener w potoku z Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a453-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="0a453-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a453-117">PARAMETERS</span></span>

### <span data-ttu-id="0a453-118">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="0a453-118">-Blob</span></span>
<span data-ttu-id="0a453-119">Określa nazwę obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="0a453-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="0a453-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a453-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0a453-121">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="0a453-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0a453-122">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="0a453-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0a453-123">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="0a453-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0a453-124">— CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0a453-124">-CloudBlob</span></span>
<span data-ttu-id="0a453-125">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a453-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="0a453-126">Aby uzyskać obiekt **CloudBlob,** użyj Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a453-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="0a453-127">- CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0a453-127">-CloudBlobContainer</span></span>
<span data-ttu-id="0a453-128">Określa obiekt **CloudBlobContainer** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a453-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="0a453-129">Możesz utworzyć obiekt lub użyć Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a453-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="0a453-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0a453-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0a453-131">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0a453-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0a453-132">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0a453-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0a453-133">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="0a453-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0a453-134">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="0a453-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0a453-135">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="0a453-135">The default value is 10.</span></span>

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

### <span data-ttu-id="0a453-136">— Kontener</span><span class="sxs-lookup"><span data-stu-id="0a453-136">-Container</span></span>
<span data-ttu-id="0a453-137">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="0a453-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="0a453-138">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0a453-138">-Context</span></span>
<span data-ttu-id="0a453-139">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a453-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0a453-140">Kontekst można utworzyć za pomocą polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a453-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0a453-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="0a453-141">-CopyId</span></span>
<span data-ttu-id="0a453-142">Określa identyfikator kopii.</span><span class="sxs-lookup"><span data-stu-id="0a453-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="0a453-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a453-143">-DefaultProfile</span></span>
<span data-ttu-id="0a453-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a453-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a453-145">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0a453-145">-Force</span></span>
<span data-ttu-id="0a453-146">Zatrzymuje bieżące zadanie kopiowania dla określonego obiektu blob bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a453-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0a453-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a453-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0a453-148">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="0a453-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0a453-149">Jeśli określony interwał pominie się przed rozpoczęciem przetwarzania żądania przez usługę magazynu, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="0a453-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0a453-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a453-150">-Confirm</span></span>
<span data-ttu-id="0a453-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a453-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a453-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a453-152">-WhatIf</span></span>
<span data-ttu-id="0a453-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a453-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a453-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0a453-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a453-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a453-155">CommonParameters</span></span>
<span data-ttu-id="0a453-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a453-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a453-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a453-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a453-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a453-158">INPUTS</span></span>

### <span data-ttu-id="0a453-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0a453-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="0a453-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0a453-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="0a453-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a453-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0a453-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a453-162">OUTPUTS</span></span>

### <span data-ttu-id="0a453-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0a453-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="0a453-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0a453-164">NOTES</span></span>

## <span data-ttu-id="0a453-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a453-165">RELATED LINKS</span></span>

[<span data-ttu-id="0a453-166">Get-AzstorageBlob</span><span class="sxs-lookup"><span data-stu-id="0a453-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="0a453-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a453-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="0a453-168">Start-AzstorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a453-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="0a453-169">Get-AzstorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="0a453-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
