---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491322"
---
# <span data-ttu-id="0fe15-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0fe15-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="0fe15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fe15-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe15-103">Umożliwia usunięcie określonego obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="0fe15-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="0fe15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fe15-104">SYNTAX</span></span>

### <span data-ttu-id="0fe15-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0fe15-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe15-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="0fe15-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0fe15-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="0fe15-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fe15-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0fe15-108">DESCRIPTION</span></span>
<span data-ttu-id="0fe15-109">Polecenie cmdlet **Remove-AzStorageBlob** umożliwia usunięcie określonego obiektu BLOB z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe15-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="0fe15-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fe15-110">EXAMPLES</span></span>

### <span data-ttu-id="0fe15-111">Przykład 1: usuwanie obiektu blob magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="0fe15-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="0fe15-112">To polecenie umożliwia usunięcie obiektu BLOB zidentyfikowanego przez jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="0fe15-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="0fe15-113">Przykład 2: usuwanie obiektu blob magazynu za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="0fe15-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="0fe15-114">To polecenie korzysta z potoku.</span><span class="sxs-lookup"><span data-stu-id="0fe15-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="0fe15-115">Przykład 3: usuwanie obiektów BLOB magazynowania za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="0fe15-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="0fe15-116">To polecenie używa symbolu wieloznacznego gwiazdki (\*) i potoku, aby pobrać obiekt BLOB lub obiekty blob, a następnie je usunąć.</span><span class="sxs-lookup"><span data-stu-id="0fe15-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="0fe15-117">Przykład 4: Usuwanie jednej wersji obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="0fe15-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="0fe15-118">To polecenie usuwa pojedyncze veriony obiekty blob z VersionId.</span><span class="sxs-lookup"><span data-stu-id="0fe15-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="0fe15-119">Przykład 5: Usuwanie pojedynczej migawki obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="0fe15-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="0fe15-120">To polecenie usuwa pojedynczą migawkę obiektów blob z SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="0fe15-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="0fe15-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fe15-121">PARAMETERS</span></span>

### <span data-ttu-id="0fe15-122">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="0fe15-122">-Blob</span></span>
<span data-ttu-id="0fe15-123">Określa nazwę obiektu BLOB, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="0fe15-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="0fe15-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0fe15-124">-BlobBaseClient</span></span>
<span data-ttu-id="0fe15-125">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0fe15-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="0fe15-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0fe15-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0fe15-127">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="0fe15-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0fe15-128">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="0fe15-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0fe15-129">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="0fe15-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0fe15-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0fe15-130">-CloudBlob</span></span>
<span data-ttu-id="0fe15-131">Określa obiekt BLOB chmury.</span><span class="sxs-lookup"><span data-stu-id="0fe15-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="0fe15-132">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="0fe15-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="0fe15-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0fe15-133">-CloudBlobContainer</span></span>
<span data-ttu-id="0fe15-134">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe15-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="0fe15-135">Możesz użyć polecenia cmdlet Get-AzStorageContainer, aby go pobrać.</span><span class="sxs-lookup"><span data-stu-id="0fe15-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="0fe15-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0fe15-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0fe15-137">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0fe15-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0fe15-138">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="0fe15-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0fe15-139">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="0fe15-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0fe15-140">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="0fe15-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0fe15-141">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="0fe15-141">The default value is 10.</span></span>

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

### <span data-ttu-id="0fe15-142">-Kontener</span><span class="sxs-lookup"><span data-stu-id="0fe15-142">-Container</span></span>
<span data-ttu-id="0fe15-143">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="0fe15-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="0fe15-144">-Context</span><span class="sxs-lookup"><span data-stu-id="0fe15-144">-Context</span></span>
<span data-ttu-id="0fe15-145">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="0fe15-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0fe15-146">Za pomocą polecenia cmdlet New-AzStorageContext możesz je utworzyć.</span><span class="sxs-lookup"><span data-stu-id="0fe15-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="0fe15-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe15-147">-DefaultProfile</span></span>
<span data-ttu-id="0fe15-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe15-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe15-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="0fe15-149">-DeleteSnapshot</span></span>
<span data-ttu-id="0fe15-150">Określa, że wszystkie migawki będą usuwane, ale nie jest bazowym obiektem BLOB.</span><span class="sxs-lookup"><span data-stu-id="0fe15-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="0fe15-151">Jeśli ten parametr nie zostanie określony, podstawowy obiekt BLOB i jego migawki zostaną usunięte razem.</span><span class="sxs-lookup"><span data-stu-id="0fe15-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="0fe15-152">Użytkownik jest monitowany o potwierdzenie operacji usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0fe15-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="0fe15-153">-Force</span><span class="sxs-lookup"><span data-stu-id="0fe15-153">-Force</span></span>
<span data-ttu-id="0fe15-154">Wskazuje, że to polecenie cmdlet usunie obiekt BLOB i jego migawkę bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="0fe15-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="0fe15-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fe15-155">-PassThru</span></span>
<span data-ttu-id="0fe15-156">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="0fe15-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0fe15-157">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="0fe15-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0fe15-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0fe15-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0fe15-159">Określa Profil platformy Azure dla polecenia cmdlet Read.</span><span class="sxs-lookup"><span data-stu-id="0fe15-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="0fe15-160">Jeśli nie określono tego parametru, polecenie cmdlet odczytuje dane z profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="0fe15-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="0fe15-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0fe15-161">-SnapshotTime</span></span>
<span data-ttu-id="0fe15-162">Obiekt BLOB SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0fe15-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="0fe15-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="0fe15-163">-VersionId</span></span>
<span data-ttu-id="0fe15-164">Obiekt BLOB VersionId</span><span class="sxs-lookup"><span data-stu-id="0fe15-164">Blob VersionId</span></span>

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

### <span data-ttu-id="0fe15-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0fe15-165">-Confirm</span></span>
<span data-ttu-id="0fe15-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fe15-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe15-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe15-167">-WhatIf</span></span>
<span data-ttu-id="0fe15-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fe15-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe15-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0fe15-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe15-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe15-170">CommonParameters</span></span>
<span data-ttu-id="0fe15-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe15-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe15-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe15-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe15-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fe15-173">INPUTS</span></span>

### <span data-ttu-id="0fe15-174">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0fe15-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="0fe15-175">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0fe15-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="0fe15-176">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0fe15-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0fe15-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fe15-177">OUTPUTS</span></span>

### <span data-ttu-id="0fe15-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fe15-178">System.Boolean</span></span>

## <span data-ttu-id="0fe15-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fe15-179">NOTES</span></span>

## <span data-ttu-id="0fe15-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fe15-180">RELATED LINKS</span></span>

[<span data-ttu-id="0fe15-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="0fe15-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="0fe15-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0fe15-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="0fe15-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0fe15-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
