---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 12bfa9ab7e35bab3421bee71cf5ea0787c95a86d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950833"
---
# <span data-ttu-id="11ae7-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="11ae7-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="11ae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="11ae7-103">Usuwa określony obiekt blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="11ae7-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="11ae7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11ae7-104">SYNTAX</span></span>

### <span data-ttu-id="11ae7-105">NamePipeline (Default)</span><span class="sxs-lookup"><span data-stu-id="11ae7-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ae7-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="11ae7-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11ae7-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="11ae7-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11ae7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="11ae7-108">DESCRIPTION</span></span>
<span data-ttu-id="11ae7-109">Polecenie **cmdlet Remove-AzStorageBlob** usuwa określony obiekt blob z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="11ae7-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="11ae7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11ae7-110">EXAMPLES</span></span>

### <span data-ttu-id="11ae7-111">Przykład 1. Usuwanie obiektu blob magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="11ae7-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="11ae7-112">To polecenie usuwa obiekt blob oznaczony jego nazwą.</span><span class="sxs-lookup"><span data-stu-id="11ae7-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="11ae7-113">Przykład 2. Usuwanie obiektu blob magazynu przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="11ae7-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="11ae7-114">To polecenie korzysta z potoku.</span><span class="sxs-lookup"><span data-stu-id="11ae7-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="11ae7-115">Przykład 3. Usuwanie obiektów blob magazynu przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="11ae7-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="11ae7-116">To polecenie używa symbolu wieloznacznego gwiazdki (\*) i potoku w celu pobrania obiektów blob lub obiektów blob, a następnie ich usuwa.</span><span class="sxs-lookup"><span data-stu-id="11ae7-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="11ae7-117">Przykład 4. Usuwanie wersji pojedynczego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="11ae7-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="11ae7-118">To polecenie usuwa pojedynczy obiekt blob o numerze VersionId.</span><span class="sxs-lookup"><span data-stu-id="11ae7-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="11ae7-119">Przykład 5. Usuwanie migawki pojedynczego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="11ae7-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="11ae7-120">To polecenie usuwa migawkę pojedynczego obiektu blob za pomocą migawki czasu migawki.</span><span class="sxs-lookup"><span data-stu-id="11ae7-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="11ae7-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11ae7-121">PARAMETERS</span></span>

### <span data-ttu-id="11ae7-122">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="11ae7-122">-Blob</span></span>
<span data-ttu-id="11ae7-123">Określa nazwę obiektu blob, który chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="11ae7-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="11ae7-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="11ae7-124">-BlobBaseClient</span></span>
<span data-ttu-id="11ae7-125">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="11ae7-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="11ae7-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11ae7-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="11ae7-127">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="11ae7-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="11ae7-128">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="11ae7-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="11ae7-129">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="11ae7-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="11ae7-130">— CloudBlob</span><span class="sxs-lookup"><span data-stu-id="11ae7-130">-CloudBlob</span></span>
<span data-ttu-id="11ae7-131">Określa obiekt blob chmury.</span><span class="sxs-lookup"><span data-stu-id="11ae7-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="11ae7-132">Aby uzyskać obiekt **CloudBlob,** użyj Get-AzStorageBlob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ae7-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="11ae7-133">- CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="11ae7-133">-CloudBlobContainer</span></span>
<span data-ttu-id="11ae7-134">Określa obiekt **CloudBlobContainer** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11ae7-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="11ae7-135">Aby go uzyskać, Get-AzStorageContainer polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ae7-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="11ae7-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="11ae7-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="11ae7-137">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="11ae7-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="11ae7-138">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="11ae7-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="11ae7-139">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="11ae7-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="11ae7-140">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="11ae7-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="11ae7-141">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="11ae7-141">The default value is 10.</span></span>

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

### <span data-ttu-id="11ae7-142">— Kontener</span><span class="sxs-lookup"><span data-stu-id="11ae7-142">-Container</span></span>
<span data-ttu-id="11ae7-143">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="11ae7-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="11ae7-144">— kontekst</span><span class="sxs-lookup"><span data-stu-id="11ae7-144">-Context</span></span>
<span data-ttu-id="11ae7-145">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11ae7-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="11ae7-146">Aby utworzyć New-AzStorageContext cmdlet, możesz użyć polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ae7-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="11ae7-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ae7-147">-DefaultProfile</span></span>
<span data-ttu-id="11ae7-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11ae7-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ae7-149">- DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="11ae7-149">-DeleteSnapshot</span></span>
<span data-ttu-id="11ae7-150">Określa, że wszystkie migawki mają zostać usunięte, ale nie obiekt blob podstawowy.</span><span class="sxs-lookup"><span data-stu-id="11ae7-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="11ae7-151">Jeśli ten parametr nie jest określony, obiekt blob podstawowy i jego migawki są usuwane razem.</span><span class="sxs-lookup"><span data-stu-id="11ae7-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="11ae7-152">Użytkownik zostanie wyświetlony monit o potwierdzenie operacji usunięcia.</span><span class="sxs-lookup"><span data-stu-id="11ae7-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="11ae7-153">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="11ae7-153">-Force</span></span>
<span data-ttu-id="11ae7-154">Wskazuje, że to polecenie cmdlet usuwa obiekt blob i jego migawkę bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="11ae7-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="11ae7-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11ae7-155">-PassThru</span></span>
<span data-ttu-id="11ae7-156">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="11ae7-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="11ae7-157">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="11ae7-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="11ae7-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11ae7-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="11ae7-159">Określa profil platformy Azure, który ma być odczytywany przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ae7-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="11ae7-160">Jeśli nie zostanie określone, polecenie cmdlet odczyta dane z profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="11ae7-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="11ae7-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="11ae7-161">-SnapshotTime</span></span>
<span data-ttu-id="11ae7-162">Migawka obiektów blob</span><span class="sxs-lookup"><span data-stu-id="11ae7-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ae7-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="11ae7-163">-VersionId</span></span>
<span data-ttu-id="11ae7-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="11ae7-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ae7-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11ae7-165">-Confirm</span></span>
<span data-ttu-id="11ae7-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11ae7-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ae7-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ae7-167">-WhatIf</span></span>
<span data-ttu-id="11ae7-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ae7-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ae7-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11ae7-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ae7-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ae7-170">CommonParameters</span></span>
<span data-ttu-id="11ae7-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ae7-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ae7-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ae7-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ae7-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ae7-173">INPUTS</span></span>

### <span data-ttu-id="11ae7-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="11ae7-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="11ae7-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="11ae7-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="11ae7-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="11ae7-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="11ae7-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ae7-177">OUTPUTS</span></span>

### <span data-ttu-id="11ae7-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11ae7-178">System.Boolean</span></span>

## <span data-ttu-id="11ae7-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11ae7-179">NOTES</span></span>

## <span data-ttu-id="11ae7-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11ae7-180">RELATED LINKS</span></span>

[<span data-ttu-id="11ae7-181">Get-AzstorageBlob</span><span class="sxs-lookup"><span data-stu-id="11ae7-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="11ae7-182">Get-AzstorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11ae7-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="11ae7-183">Set-AzstorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11ae7-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
