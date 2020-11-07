---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageblob
schema: 2.0.0
ms.openlocfilehash: 2b0179006f64f94d94d11c2a1fd8159d1cbeefde
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897710"
---
# <span data-ttu-id="a9d36-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a9d36-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="a9d36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9d36-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d36-103">Umożliwia usunięcie określonego obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="a9d36-103">Removes the specified storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9d36-104">SYNTAX</span></span>

### <span data-ttu-id="a9d36-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9d36-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d36-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a9d36-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d36-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a9d36-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9d36-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9d36-108">DESCRIPTION</span></span>
<span data-ttu-id="a9d36-109">Polecenie cmdlet **Remove-AzureStorageBlob** umożliwia usunięcie określonego obiektu BLOB z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d36-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="a9d36-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9d36-110">EXAMPLES</span></span>

### <span data-ttu-id="a9d36-111">Przykład 1: usuwanie obiektu blob magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="a9d36-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="a9d36-112">To polecenie umożliwia usunięcie obiektu BLOB zidentyfikowanego przez jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="a9d36-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="a9d36-113">Przykład 2: usuwanie obiektu blob magazynu za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="a9d36-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="a9d36-114">To polecenie korzysta z potoku.</span><span class="sxs-lookup"><span data-stu-id="a9d36-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="a9d36-115">Przykład 3: usuwanie obiektów BLOB magazynowania za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="a9d36-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="a9d36-116">To polecenie używa symbolu wieloznacznego gwiazdki (\*) i potoku, aby pobrać obiekt BLOB lub obiekty blob, a następnie je usunąć.</span><span class="sxs-lookup"><span data-stu-id="a9d36-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="a9d36-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9d36-117">PARAMETERS</span></span>

### <span data-ttu-id="a9d36-118">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="a9d36-118">-Blob</span></span>
<span data-ttu-id="a9d36-119">Określa nazwę obiektu BLOB, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a9d36-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="a9d36-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9d36-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a9d36-121">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="a9d36-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a9d36-122">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="a9d36-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a9d36-123">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="a9d36-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a9d36-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a9d36-124">-CloudBlob</span></span>
<span data-ttu-id="a9d36-125">Określa obiekt BLOB chmury.</span><span class="sxs-lookup"><span data-stu-id="a9d36-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="a9d36-126">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="a9d36-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a9d36-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a9d36-127">-CloudBlobContainer</span></span>
<span data-ttu-id="a9d36-128">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d36-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a9d36-129">Możesz użyć polecenia cmdlet Get-AzureStorageContainer, aby go pobrać.</span><span class="sxs-lookup"><span data-stu-id="a9d36-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="a9d36-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a9d36-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a9d36-131">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a9d36-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a9d36-132">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a9d36-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a9d36-133">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="a9d36-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a9d36-134">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="a9d36-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a9d36-135">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a9d36-135">The default value is 10.</span></span>

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

### <span data-ttu-id="a9d36-136">-Kontener</span><span class="sxs-lookup"><span data-stu-id="a9d36-136">-Container</span></span>
<span data-ttu-id="a9d36-137">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="a9d36-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="a9d36-138">-Context</span><span class="sxs-lookup"><span data-stu-id="a9d36-138">-Context</span></span>
<span data-ttu-id="a9d36-139">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a9d36-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a9d36-140">Za pomocą polecenia cmdlet New-AzureStorageContext możesz je utworzyć.</span><span class="sxs-lookup"><span data-stu-id="a9d36-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="a9d36-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d36-141">-DefaultProfile</span></span>
<span data-ttu-id="a9d36-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d36-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d36-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="a9d36-143">-DeleteSnapshot</span></span>
<span data-ttu-id="a9d36-144">Określa, że wszystkie migawki będą usuwane, ale nie jest bazowym obiektem BLOB.</span><span class="sxs-lookup"><span data-stu-id="a9d36-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="a9d36-145">Jeśli ten parametr nie zostanie określony, podstawowy obiekt BLOB i jego migawki zostaną usunięte razem.</span><span class="sxs-lookup"><span data-stu-id="a9d36-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="a9d36-146">Użytkownik jest monitowany o potwierdzenie operacji usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a9d36-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="a9d36-147">-Force</span><span class="sxs-lookup"><span data-stu-id="a9d36-147">-Force</span></span>
<span data-ttu-id="a9d36-148">Wskazuje, że to polecenie cmdlet usunie obiekt BLOB i jego migawkę bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a9d36-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="a9d36-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9d36-149">-PassThru</span></span>
<span data-ttu-id="a9d36-150">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="a9d36-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a9d36-151">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="a9d36-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a9d36-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9d36-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a9d36-153">Określa Profil platformy Azure dla polecenia cmdlet Read.</span><span class="sxs-lookup"><span data-stu-id="a9d36-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="a9d36-154">Jeśli nie określono tego parametru, polecenie cmdlet odczytuje dane z profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="a9d36-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="a9d36-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9d36-155">-Confirm</span></span>
<span data-ttu-id="a9d36-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d36-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d36-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d36-157">-WhatIf</span></span>
<span data-ttu-id="a9d36-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d36-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d36-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9d36-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d36-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d36-160">CommonParameters</span></span>
<span data-ttu-id="a9d36-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d36-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d36-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d36-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d36-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9d36-163">INPUTS</span></span>

### <span data-ttu-id="a9d36-164">Microsoft. platformy windowsazure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a9d36-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a9d36-165">Microsoft. platformy windowsazure. Storage. blob. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a9d36-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a9d36-166">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9d36-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9d36-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9d36-167">OUTPUTS</span></span>

### <span data-ttu-id="a9d36-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9d36-168">System.Boolean</span></span>

## <span data-ttu-id="a9d36-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9d36-169">NOTES</span></span>

## <span data-ttu-id="a9d36-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9d36-170">RELATED LINKS</span></span>

[<span data-ttu-id="a9d36-171">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a9d36-171">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="a9d36-172">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a9d36-172">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="a9d36-173">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a9d36-173">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
