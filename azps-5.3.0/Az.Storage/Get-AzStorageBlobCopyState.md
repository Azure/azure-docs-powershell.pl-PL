---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489309"
---
# <span data-ttu-id="69819-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="69819-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="69819-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69819-102">SYNOPSIS</span></span>
<span data-ttu-id="69819-103">Pobiera stan kopii obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69819-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="69819-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69819-104">SYNTAX</span></span>

### <span data-ttu-id="69819-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69819-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="69819-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="69819-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="69819-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="69819-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="69819-108">Opis</span><span class="sxs-lookup"><span data-stu-id="69819-108">DESCRIPTION</span></span>
<span data-ttu-id="69819-109">Polecenie cmdlet **Get-AzStorageBlobCopyState** Pobiera stan kopii obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="69819-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="69819-110">Należy go uruchomić na docelowym obiekcie blob kopiowania.</span><span class="sxs-lookup"><span data-stu-id="69819-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="69819-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69819-111">EXAMPLES</span></span>

### <span data-ttu-id="69819-112">Przykład 1. Pobieranie stanu kopii obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="69819-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="69819-113">To polecenie pobiera stan kopii obiektu BLOB o nazwie ContosoPlanning2015 w ContosoUploads kontenera.</span><span class="sxs-lookup"><span data-stu-id="69819-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="69819-114">Przykład 2: pobieranie stanu kopiowania obiektu BLOB za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="69819-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="69819-115">To polecenie pobiera obiekt BLOB o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads przy użyciu polecenia cmdlet **Get-AzStorageBlob** , a następnie przekazuje wynik do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="69819-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="69819-116">Polecenie cmdlet **Get-AzStorageBlobCopyState** Pobiera stan kopii tego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="69819-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="69819-117">Przykład 3: pobieranie stanu kopiowania obiektu BLOB w kontenerze za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="69819-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="69819-118">To polecenie uzyskuje kontener o nazwie za pomocą polecenia cmdlet **Get-AzStorageBlob** , a następnie przekazuje wynik do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69819-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="69819-119">Polecenie cmdlet **Get-AzStorageContainer** Pobiera stan kopii obiektu BLOB o nazwie ContosoPlanning2015 w tym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="69819-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="69819-120">Przykład 4: Rozpoczynanie kopiowania i potoku w celu uzyskania statusu kopii</span><span class="sxs-lookup"><span data-stu-id="69819-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="69819-121">Pierwsze polecenie rozpoczyna Kopiowanie obiektu BLOB "ContosoPlanning2015" do "ContosoPlanning2015_copy", a następnie wyprowadza obiekt BLOB destiantion.</span><span class="sxs-lookup"><span data-stu-id="69819-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="69819-122">Drugie polecenie podaje obiekt BLOB destiantion, aby uzyskać-AzStorageBlobCopyState, aby uzyskać stan kopii obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="69819-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="69819-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69819-123">PARAMETERS</span></span>

### <span data-ttu-id="69819-124">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="69819-124">-Blob</span></span>
<span data-ttu-id="69819-125">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="69819-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="69819-126">To polecenie cmdlet pobiera stan operacji kopiowania obiektu BLOB dla obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="69819-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="69819-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="69819-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="69819-128">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="69819-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="69819-129">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="69819-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="69819-130">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="69819-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="69819-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="69819-131">-CloudBlob</span></span>
<span data-ttu-id="69819-132">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69819-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="69819-133">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="69819-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="69819-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="69819-134">-CloudBlobContainer</span></span>
<span data-ttu-id="69819-135">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69819-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="69819-136">To polecenie cmdlet pobiera stan kopii obiektu BLOB w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="69819-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="69819-137">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="69819-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="69819-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="69819-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="69819-139">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="69819-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="69819-140">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="69819-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="69819-141">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="69819-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="69819-142">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="69819-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="69819-143">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="69819-143">The default value is 10.</span></span>

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

### <span data-ttu-id="69819-144">-Kontener</span><span class="sxs-lookup"><span data-stu-id="69819-144">-Container</span></span>
<span data-ttu-id="69819-145">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="69819-145">Specifies the name of a container.</span></span>
<span data-ttu-id="69819-146">To polecenie cmdlet pobiera stan kopii obiektu BLOB w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="69819-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="69819-147">-Context</span><span class="sxs-lookup"><span data-stu-id="69819-147">-Context</span></span>
<span data-ttu-id="69819-148">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="69819-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="69819-149">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="69819-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="69819-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69819-150">-DefaultProfile</span></span>
<span data-ttu-id="69819-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69819-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69819-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="69819-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="69819-153">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="69819-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="69819-154">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="69819-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="69819-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="69819-155">-WaitForComplete</span></span>
<span data-ttu-id="69819-156">Wskazuje, że to polecenie cmdlet oczekuje na zakończenie kopii.</span><span class="sxs-lookup"><span data-stu-id="69819-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="69819-157">Jeśli nie podano tego parametru, to polecenie cmdlet natychmiast zwraca wynik.</span><span class="sxs-lookup"><span data-stu-id="69819-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="69819-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69819-158">CommonParameters</span></span>
<span data-ttu-id="69819-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69819-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69819-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69819-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69819-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69819-161">INPUTS</span></span>

### <span data-ttu-id="69819-162">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="69819-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="69819-163">Microsoft. Azure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="69819-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="69819-164">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="69819-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="69819-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69819-165">OUTPUTS</span></span>

### <span data-ttu-id="69819-166">Microsoft. Azure. Storage. blob. CopyState</span><span class="sxs-lookup"><span data-stu-id="69819-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="69819-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69819-167">NOTES</span></span>

## <span data-ttu-id="69819-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69819-168">RELATED LINKS</span></span>

[<span data-ttu-id="69819-169">Start — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="69819-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="69819-170">Zatrzymaj — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="69819-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


