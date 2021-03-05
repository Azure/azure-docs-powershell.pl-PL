---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 4bc06ca07c95986f75062a64a0f86475f7720ff1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002746"
---
# <span data-ttu-id="17fbc-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="17fbc-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="17fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="17fbc-103">Pobiera stan kopii obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17fbc-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="17fbc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17fbc-104">SYNTAX</span></span>

### <span data-ttu-id="17fbc-105">NamePipeline (Default)</span><span class="sxs-lookup"><span data-stu-id="17fbc-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="17fbc-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="17fbc-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="17fbc-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="17fbc-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="17fbc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="17fbc-108">DESCRIPTION</span></span>
<span data-ttu-id="17fbc-109">Polecenie **cmdlet Get-AzStorageBlobCopyState** pobiera stan kopii obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17fbc-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="17fbc-110">Powinna zostać ona uruchamiana w obiekcie blob kopiowania miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="17fbc-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="17fbc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17fbc-111">EXAMPLES</span></span>

### <span data-ttu-id="17fbc-112">Przykład 1. Uzyskiwanie stanu kopii obiektu blob</span><span class="sxs-lookup"><span data-stu-id="17fbc-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="17fbc-113">To polecenie pobiera stan kopii obiektu blob o nazwie ContosoPlanning2015 w kontenerze ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="17fbc-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="17fbc-114">Przykład 2. Uzyskiwanie stanu kopii obiektu blob przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="17fbc-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="17fbc-115">To polecenie pobiera obiekt blob o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads przy użyciu polecenia cmdlet **Get-AzStorageBlob,** a następnie przekazuje wynik do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="17fbc-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="17fbc-116">Polecenie **cmdlet Get-AzStorageBlobCopyState** pobiera stan kopii dla tego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="17fbc-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="17fbc-117">Przykład 3. Uzyskiwanie stanu kopii obiektu blob w kontenerze przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="17fbc-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="17fbc-118">To polecenie pobiera kontener o nazwie za pomocą polecenia cmdlet **Get-AzStorageBlob,** a następnie przekazuje wynik do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fbc-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="17fbc-119">Polecenie **cmdlet Get-AzStorageContainer** pobiera stan kopii dla obiektu blob o nazwie ContosoPlanning2015 w tym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="17fbc-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="17fbc-120">Przykład 4. Uruchamianie kopiowania i potoku w celu uzyskania stanu kopiowania</span><span class="sxs-lookup"><span data-stu-id="17fbc-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="17fbc-121">Pierwsze polecenie uruchamia kopiowanie obiektu blob "ContosoPlanning2015" do "ContosoPlanning2015_copy", a następnie wyprowadza obiekt blob destion.</span><span class="sxs-lookup"><span data-stu-id="17fbc-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="17fbc-122">Drugi potok polecenia obiekt blob destion do Get-AzStorageBlobCopyState w celu uzyskania stanu kopiowania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="17fbc-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="17fbc-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17fbc-123">PARAMETERS</span></span>

### <span data-ttu-id="17fbc-124">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="17fbc-124">-Blob</span></span>
<span data-ttu-id="17fbc-125">Określa nazwę obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="17fbc-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="17fbc-126">To polecenie cmdlet pobiera stan operacji kopiowania obiektów blob dla obiektu blob magazynu platformy Azure, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="17fbc-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="17fbc-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="17fbc-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="17fbc-128">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="17fbc-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="17fbc-129">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="17fbc-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="17fbc-130">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="17fbc-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="17fbc-131">— CloudBlob</span><span class="sxs-lookup"><span data-stu-id="17fbc-131">-CloudBlob</span></span>
<span data-ttu-id="17fbc-132">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17fbc-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="17fbc-133">Aby uzyskać obiekt **CloudBlob,** użyj Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fbc-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="17fbc-134">- CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="17fbc-134">-CloudBlobContainer</span></span>
<span data-ttu-id="17fbc-135">Określa obiekt **CloudBlobContainer** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17fbc-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="17fbc-136">To polecenie cmdlet pobiera stan kopii obiektu blob w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="17fbc-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="17fbc-137">Aby uzyskać obiekt **CloudBlobContainer,** użyj Get-AzStorageContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fbc-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="17fbc-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="17fbc-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="17fbc-139">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="17fbc-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="17fbc-140">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="17fbc-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="17fbc-141">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="17fbc-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="17fbc-142">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="17fbc-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="17fbc-143">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="17fbc-143">The default value is 10.</span></span>

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

### <span data-ttu-id="17fbc-144">— Kontener</span><span class="sxs-lookup"><span data-stu-id="17fbc-144">-Container</span></span>
<span data-ttu-id="17fbc-145">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="17fbc-145">Specifies the name of a container.</span></span>
<span data-ttu-id="17fbc-146">To polecenie cmdlet pobiera stan kopii dla obiektu blob w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="17fbc-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="17fbc-147">— kontekst</span><span class="sxs-lookup"><span data-stu-id="17fbc-147">-Context</span></span>
<span data-ttu-id="17fbc-148">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17fbc-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="17fbc-149">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fbc-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="17fbc-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fbc-150">-DefaultProfile</span></span>
<span data-ttu-id="17fbc-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17fbc-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17fbc-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="17fbc-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="17fbc-153">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="17fbc-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="17fbc-154">Jeśli określony interwał pominie się przed rozpoczęciem przetwarzania żądania przez usługę magazynu, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="17fbc-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="17fbc-155">- WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="17fbc-155">-WaitForComplete</span></span>
<span data-ttu-id="17fbc-156">Wskazuje, że to polecenie cmdlet czeka na ukończenie kopii.</span><span class="sxs-lookup"><span data-stu-id="17fbc-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="17fbc-157">Jeśli nie określisz tego parametru, to polecenie cmdlet natychmiast zwróci wynik.</span><span class="sxs-lookup"><span data-stu-id="17fbc-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="17fbc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fbc-158">CommonParameters</span></span>
<span data-ttu-id="17fbc-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17fbc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fbc-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fbc-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fbc-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17fbc-161">INPUTS</span></span>

### <span data-ttu-id="17fbc-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="17fbc-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="17fbc-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="17fbc-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="17fbc-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="17fbc-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="17fbc-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17fbc-165">OUTPUTS</span></span>

### <span data-ttu-id="17fbc-166">Microsoft.Azure.Storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="17fbc-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="17fbc-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17fbc-167">NOTES</span></span>

## <span data-ttu-id="17fbc-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17fbc-168">RELATED LINKS</span></span>

[<span data-ttu-id="17fbc-169">Start-AzstorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="17fbc-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="17fbc-170">Stop-AzstorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="17fbc-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


