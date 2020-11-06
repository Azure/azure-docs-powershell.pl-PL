---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
ms.openlocfilehash: 45368a3abe428c65604d4ba103cf793972e50ea1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545940"
---
# <span data-ttu-id="eafce-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eafce-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="eafce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eafce-102">SYNOPSIS</span></span>
<span data-ttu-id="eafce-103">Zawiera listę kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="eafce-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eafce-104">SYNTAX</span></span>

### <span data-ttu-id="eafce-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="eafce-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eafce-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="eafce-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="eafce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eafce-107">DESCRIPTION</span></span>
<span data-ttu-id="eafce-108">Polecenie cmdlet **Get-AzureStorageContainer** zawiera listę kontenerów magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="eafce-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="eafce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eafce-109">EXAMPLES</span></span>

### <span data-ttu-id="eafce-110">Przykład 1: Pobieranie obiektu blob magazynu platformy Azure według nazwy</span><span class="sxs-lookup"><span data-stu-id="eafce-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="eafce-111">W tym przykładzie użyto symbolu wieloznacznego w celu zwrócenia listy wszystkich kontenerów o nazwie rozpoczynającej się od kontenera.</span><span class="sxs-lookup"><span data-stu-id="eafce-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="eafce-112">Przykład 2: uzyskiwanie prefiksu nazwy kontenera usługi Azure Storage kontener</span><span class="sxs-lookup"><span data-stu-id="eafce-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="eafce-113">W tym przykładzie użyto parametru *prefix* w celu zwrócenia listy wszystkich kontenerów o nazwie rozpoczynającej się od kontenera.</span><span class="sxs-lookup"><span data-stu-id="eafce-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="eafce-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eafce-114">PARAMETERS</span></span>

### <span data-ttu-id="eafce-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eafce-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eafce-116">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="eafce-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eafce-117">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="eafce-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eafce-118">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="eafce-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eafce-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eafce-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eafce-120">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="eafce-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eafce-121">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="eafce-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eafce-122">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="eafce-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eafce-123">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="eafce-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eafce-124">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="eafce-124">The default value is 10.</span></span>

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

### <span data-ttu-id="eafce-125">-Context</span><span class="sxs-lookup"><span data-stu-id="eafce-125">-Context</span></span>
<span data-ttu-id="eafce-126">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="eafce-126">Specifies the storage context.</span></span>
<span data-ttu-id="eafce-127">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eafce-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="eafce-128">Polecenie cmdlet nie powiedzie się, gdy użyjesz kontekstu magazynowania utworzonego na podstawie tokenu SAS, ponieważ polecenie cmdlet będzie wysyłać kwerendy dotyczące uprawnień kontenera, które wymagają uprawnień klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="eafce-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="eafce-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="eafce-129">-ContinuationToken</span></span>
<span data-ttu-id="eafce-130">Określa token kontynuacji listy obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="eafce-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafce-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eafce-131">-MaxCount</span></span>
<span data-ttu-id="eafce-132">Określa maksymalną liczbę obiektów, które zostanie zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eafce-132">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="eafce-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eafce-133">-Name</span></span>
<span data-ttu-id="eafce-134">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="eafce-134">Specifies the container name.</span></span>
<span data-ttu-id="eafce-135">Jeśli nazwa kontenera jest pusta, polecenie cmdlet wyświetla wszystkie kontenery.</span><span class="sxs-lookup"><span data-stu-id="eafce-135">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="eafce-136">W przeciwnym razie wyświetla wszystkie kontenery zgodne z określoną nazwą lub wzorcem zwykłej nazwy.</span><span class="sxs-lookup"><span data-stu-id="eafce-136">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="eafce-137">-Prefix</span><span class="sxs-lookup"><span data-stu-id="eafce-137">-Prefix</span></span>
<span data-ttu-id="eafce-138">Określa prefiks stosowany w nazwie kontenera lub kontenerów, które mają zostać przeszukane.</span><span class="sxs-lookup"><span data-stu-id="eafce-138">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="eafce-139">Za pomocą tej pozycji można znaleźć wszystkie kontenery, które zaczynają się od tego samego ciągu, na przykład "my" lub "test".</span><span class="sxs-lookup"><span data-stu-id="eafce-139">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafce-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eafce-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eafce-141">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="eafce-141">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="eafce-142">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="eafce-142">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="eafce-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafce-143">CommonParameters</span></span>
<span data-ttu-id="eafce-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafce-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafce-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafce-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafce-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eafce-146">INPUTS</span></span>

### <span data-ttu-id="eafce-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eafce-147">IStorageContext</span></span>

<span data-ttu-id="eafce-148">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="eafce-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="eafce-149">Ciąg</span><span class="sxs-lookup"><span data-stu-id="eafce-149">String</span></span>

<span data-ttu-id="eafce-150">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="eafce-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="eafce-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eafce-151">OUTPUTS</span></span>

### <span data-ttu-id="eafce-152">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eafce-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="eafce-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eafce-153">NOTES</span></span>

## <span data-ttu-id="eafce-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eafce-154">RELATED LINKS</span></span>

[<span data-ttu-id="eafce-155">Nowe — AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eafce-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="eafce-156">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eafce-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="eafce-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="eafce-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


