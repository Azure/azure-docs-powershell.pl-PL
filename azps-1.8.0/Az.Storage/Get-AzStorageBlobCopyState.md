---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 37722669af74fdc6032efdcd98f890585bde6847
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707638"
---
# <span data-ttu-id="6ee69-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="6ee69-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="6ee69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ee69-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee69-103">Pobiera stan kopii obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee69-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="6ee69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ee69-104">SYNTAX</span></span>

### <span data-ttu-id="6ee69-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ee69-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6ee69-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6ee69-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6ee69-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6ee69-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6ee69-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ee69-108">DESCRIPTION</span></span>
<span data-ttu-id="6ee69-109">Polecenie cmdlet **Get-AzStorageBlobCopyState** Pobiera stan kopii obiektu BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6ee69-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="6ee69-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ee69-110">EXAMPLES</span></span>

### <span data-ttu-id="6ee69-111">Przykład 1. Pobieranie stanu kopii obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="6ee69-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="6ee69-112">To polecenie pobiera stan kopii obiektu BLOB o nazwie ContosoPlanning2015 w ContosoUploads kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ee69-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="6ee69-113">Przykład 2: pobieranie stanu kopiowania obiektu BLOB za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="6ee69-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="6ee69-114">To polecenie pobiera obiekt BLOB o nazwie ContosoPlanning2015 w kontenerze o nazwie ContosoUploads przy użyciu polecenia cmdlet **Get-AzStorageBlob** , a następnie przekazuje wynik do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6ee69-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ee69-115">Polecenie cmdlet **Get-AzStorageBlobCopyState** Pobiera stan kopii tego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6ee69-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="6ee69-116">Przykład 3: pobieranie stanu kopiowania obiektu BLOB w kontenerze za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="6ee69-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="6ee69-117">To polecenie uzyskuje kontener o nazwie za pomocą polecenia cmdlet **Get-AzStorageBlob** , a następnie przekazuje wynik do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ee69-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="6ee69-118">Polecenie cmdlet **Get-AzStorageContainer** Pobiera stan kopii obiektu BLOB o nazwie ContosoPlanning2015 w tym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="6ee69-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="6ee69-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ee69-119">PARAMETERS</span></span>

### <span data-ttu-id="6ee69-120">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="6ee69-120">-Blob</span></span>
<span data-ttu-id="6ee69-121">Określa nazwę obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6ee69-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="6ee69-122">To polecenie cmdlet pobiera stan operacji kopiowania obiektu BLOB dla obiektu BLOB usługi Azure Storage, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6ee69-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ee69-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ee69-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6ee69-124">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="6ee69-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6ee69-125">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="6ee69-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6ee69-126">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="6ee69-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6ee69-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ee69-127">-CloudBlob</span></span>
<span data-ttu-id="6ee69-128">Określa obiekt **CloudBlob** z biblioteki klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee69-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="6ee69-129">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="6ee69-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6ee69-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6ee69-130">-CloudBlobContainer</span></span>
<span data-ttu-id="6ee69-131">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee69-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6ee69-132">To polecenie cmdlet pobiera stan kopii obiektu BLOB w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6ee69-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="6ee69-133">Aby uzyskać obiekt **CloudBlobContainer** , użyj polecenia cmdlet Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="6ee69-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6ee69-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ee69-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ee69-135">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6ee69-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6ee69-136">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6ee69-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6ee69-137">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="6ee69-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6ee69-138">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="6ee69-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6ee69-139">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="6ee69-139">The default value is 10.</span></span>

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

### <span data-ttu-id="6ee69-140">-Kontener</span><span class="sxs-lookup"><span data-stu-id="6ee69-140">-Container</span></span>
<span data-ttu-id="6ee69-141">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ee69-141">Specifies the name of a container.</span></span>
<span data-ttu-id="6ee69-142">To polecenie cmdlet pobiera stan kopii obiektu BLOB w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6ee69-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ee69-143">-Context</span><span class="sxs-lookup"><span data-stu-id="6ee69-143">-Context</span></span>
<span data-ttu-id="6ee69-144">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6ee69-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ee69-145">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6ee69-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6ee69-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee69-146">-DefaultProfile</span></span>
<span data-ttu-id="6ee69-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee69-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ee69-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ee69-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6ee69-149">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="6ee69-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6ee69-150">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="6ee69-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6ee69-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6ee69-151">-WaitForComplete</span></span>
<span data-ttu-id="6ee69-152">Wskazuje, że to polecenie cmdlet oczekuje na zakończenie kopii.</span><span class="sxs-lookup"><span data-stu-id="6ee69-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="6ee69-153">Jeśli nie podano tego parametru, to polecenie cmdlet natychmiast zwraca wynik.</span><span class="sxs-lookup"><span data-stu-id="6ee69-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="6ee69-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee69-154">CommonParameters</span></span>
<span data-ttu-id="6ee69-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee69-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee69-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee69-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee69-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ee69-157">INPUTS</span></span>

### <span data-ttu-id="6ee69-158">Microsoft. platformy windowsazure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6ee69-158">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6ee69-159">Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6ee69-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6ee69-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ee69-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ee69-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ee69-161">OUTPUTS</span></span>

### <span data-ttu-id="6ee69-162">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6ee69-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6ee69-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ee69-163">NOTES</span></span>

## <span data-ttu-id="6ee69-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ee69-164">RELATED LINKS</span></span>

[<span data-ttu-id="6ee69-165">Start — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ee69-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="6ee69-166">Zatrzymaj — AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ee69-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


