---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b40585f584cc8c2634acab54e6862e4163c6b7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523745"
---
# <span data-ttu-id="85433-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="85433-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="85433-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85433-102">SYNOPSIS</span></span>
<span data-ttu-id="85433-103">Umożliwia usunięcie określonego obiektu blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="85433-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="85433-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85433-104">SYNTAX</span></span>

### <span data-ttu-id="85433-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85433-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85433-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="85433-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85433-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="85433-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85433-108">Opis</span><span class="sxs-lookup"><span data-stu-id="85433-108">DESCRIPTION</span></span>
<span data-ttu-id="85433-109">Polecenie cmdlet **Remove-AzureStorageBlob** umożliwia usunięcie określonego obiektu BLOB z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="85433-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="85433-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85433-110">EXAMPLES</span></span>

### <span data-ttu-id="85433-111">Przykład 1: usuwanie obiektu blob magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="85433-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="85433-112">To polecenie umożliwia usunięcie obiektu BLOB zidentyfikowanego przez jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="85433-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="85433-113">Przykład 2: usuwanie obiektu blob magazynu za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="85433-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="85433-114">To polecenie korzysta z potoku.</span><span class="sxs-lookup"><span data-stu-id="85433-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="85433-115">Przykład 3: usuwanie obiektów BLOB magazynowania za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="85433-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="85433-116">To polecenie używa symbolu wieloznacznego gwiazdki (\*) i potoku, aby pobrać obiekt BLOB lub obiekty blob, a następnie je usunąć.</span><span class="sxs-lookup"><span data-stu-id="85433-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="85433-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85433-117">PARAMETERS</span></span>

### <span data-ttu-id="85433-118">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="85433-118">-Blob</span></span>
<span data-ttu-id="85433-119">Określa nazwę obiektu BLOB, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="85433-119">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="85433-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="85433-121">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="85433-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="85433-122">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="85433-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="85433-123">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="85433-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="85433-124">-CloudBlob</span></span>
<span data-ttu-id="85433-125">Określa obiekt BLOB chmury.</span><span class="sxs-lookup"><span data-stu-id="85433-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="85433-126">Aby uzyskać obiekt **CloudBlob** , użyj polecenia cmdlet Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="85433-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85433-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="85433-127">-CloudBlobContainer</span></span>
<span data-ttu-id="85433-128">Określa obiekt **CloudBlobContainer** w bibliotece klienta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85433-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="85433-129">Możesz użyć polecenia cmdlet Get-AzureStorageContainer, aby go pobrać.</span><span class="sxs-lookup"><span data-stu-id="85433-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85433-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="85433-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="85433-131">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="85433-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="85433-132">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="85433-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="85433-133">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="85433-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="85433-134">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="85433-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="85433-135">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="85433-135">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-136">-Kontener</span><span class="sxs-lookup"><span data-stu-id="85433-136">-Container</span></span>
<span data-ttu-id="85433-137">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="85433-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-138">-Context</span><span class="sxs-lookup"><span data-stu-id="85433-138">-Context</span></span>
<span data-ttu-id="85433-139">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="85433-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="85433-140">Za pomocą polecenia cmdlet New-AzureStorageContext możesz je utworzyć.</span><span class="sxs-lookup"><span data-stu-id="85433-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85433-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="85433-141">-DeleteSnapshot</span></span>
<span data-ttu-id="85433-142">Określa, że wszystkie migawki będą usuwane, ale nie jest bazowym obiektem BLOB.</span><span class="sxs-lookup"><span data-stu-id="85433-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="85433-143">Jeśli ten parametr nie zostanie określony, podstawowy obiekt BLOB i jego migawki zostaną usunięte razem.</span><span class="sxs-lookup"><span data-stu-id="85433-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="85433-144">Użytkownik jest monitowany o potwierdzenie operacji usunięcia.</span><span class="sxs-lookup"><span data-stu-id="85433-144">The user is prompted to confirm the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-145">-Force</span><span class="sxs-lookup"><span data-stu-id="85433-145">-Force</span></span>
<span data-ttu-id="85433-146">Wskazuje, że to polecenie cmdlet usunie obiekt BLOB i jego migawkę bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="85433-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85433-147">-PassThru</span></span>
<span data-ttu-id="85433-148">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="85433-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="85433-149">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="85433-149">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="85433-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="85433-151">Określa Profil platformy Azure dla polecenia cmdlet Read.</span><span class="sxs-lookup"><span data-stu-id="85433-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="85433-152">Jeśli nie określono tego parametru, polecenie cmdlet odczytuje dane z profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="85433-152">If not specified, the cmdlet reads from the default profile.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85433-153">-Confirm</span></span>
<span data-ttu-id="85433-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85433-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85433-155">-WhatIf</span></span>
<span data-ttu-id="85433-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85433-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85433-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85433-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85433-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85433-158">CommonParameters</span></span>
<span data-ttu-id="85433-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85433-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85433-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85433-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85433-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85433-161">INPUTS</span></span>

## <span data-ttu-id="85433-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85433-162">OUTPUTS</span></span>

## <span data-ttu-id="85433-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85433-163">NOTES</span></span>

## <span data-ttu-id="85433-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85433-164">RELATED LINKS</span></span>

[<span data-ttu-id="85433-165">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="85433-165">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="85433-166">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="85433-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="85433-167">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="85433-167">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
