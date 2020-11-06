---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: c94c9b9d04745fe22c8836be1858c59c253d4b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550163"
---
# <span data-ttu-id="d2a44-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d2a44-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="d2a44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2a44-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a44-103">Zawiera listę kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="d2a44-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2a44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2a44-104">SYNTAX</span></span>

### <span data-ttu-id="d2a44-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d2a44-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d2a44-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="d2a44-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d2a44-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d2a44-107">DESCRIPTION</span></span>
<span data-ttu-id="d2a44-108">Polecenie cmdlet **Get-AzureStorageContainer** zawiera listę kontenerów magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a44-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d2a44-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2a44-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a44-110">Przykład 1: Pobieranie obiektu blob magazynu platformy Azure według nazwy</span><span class="sxs-lookup"><span data-stu-id="d2a44-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="d2a44-111">W tym przykładzie użyto symbolu wieloznacznego w celu zwrócenia listy wszystkich kontenerów o nazwie rozpoczynającej się od kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2a44-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="d2a44-112">Przykład 2: uzyskiwanie prefiksu nazwy kontenera usługi Azure Storage kontener</span><span class="sxs-lookup"><span data-stu-id="d2a44-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="d2a44-113">W tym przykładzie użyto parametru *prefix* w celu zwrócenia listy wszystkich kontenerów o nazwie rozpoczynającej się od kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2a44-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="d2a44-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2a44-114">PARAMETERS</span></span>

### <span data-ttu-id="d2a44-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d2a44-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d2a44-116">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="d2a44-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d2a44-117">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="d2a44-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d2a44-118">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="d2a44-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d2a44-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d2a44-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d2a44-120">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="d2a44-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d2a44-121">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="d2a44-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d2a44-122">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="d2a44-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d2a44-123">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="d2a44-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d2a44-124">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="d2a44-124">The default value is 10.</span></span>

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

### <span data-ttu-id="d2a44-125">-Context</span><span class="sxs-lookup"><span data-stu-id="d2a44-125">-Context</span></span>
<span data-ttu-id="d2a44-126">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d2a44-126">Specifies the storage context.</span></span>
<span data-ttu-id="d2a44-127">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2a44-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d2a44-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="d2a44-128">-ContinuationToken</span></span>
<span data-ttu-id="d2a44-129">Określa token kontynuacji listy obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="d2a44-129">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="d2a44-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d2a44-130">-MaxCount</span></span>
<span data-ttu-id="d2a44-131">Określa maksymalną liczbę obiektów, które zostanie zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2a44-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="d2a44-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2a44-132">-Name</span></span>
<span data-ttu-id="d2a44-133">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2a44-133">Specifies the container name.</span></span>
<span data-ttu-id="d2a44-134">Jeśli nazwa kontenera jest pusta, polecenie cmdlet wyświetla wszystkie kontenery.</span><span class="sxs-lookup"><span data-stu-id="d2a44-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="d2a44-135">W przeciwnym razie wyświetla wszystkie kontenery zgodne z określoną nazwą lub wzorcem zwykłej nazwy.</span><span class="sxs-lookup"><span data-stu-id="d2a44-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="d2a44-136">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d2a44-136">-Prefix</span></span>
<span data-ttu-id="d2a44-137">Określa prefiks stosowany w nazwie kontenera lub kontenerów, które mają zostać przeszukane.</span><span class="sxs-lookup"><span data-stu-id="d2a44-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="d2a44-138">Za pomocą tej pozycji można znaleźć wszystkie kontenery, które zaczynają się od tego samego ciągu, na przykład "my" lub "test".</span><span class="sxs-lookup"><span data-stu-id="d2a44-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="d2a44-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d2a44-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d2a44-140">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="d2a44-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d2a44-141">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="d2a44-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d2a44-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a44-142">CommonParameters</span></span>
<span data-ttu-id="d2a44-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a44-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a44-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a44-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a44-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2a44-145">INPUTS</span></span>

### <span data-ttu-id="d2a44-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d2a44-146">IStorageContext</span></span>

<span data-ttu-id="d2a44-147">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="d2a44-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d2a44-148">Ciąg</span><span class="sxs-lookup"><span data-stu-id="d2a44-148">String</span></span>

<span data-ttu-id="d2a44-149">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="d2a44-149">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d2a44-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2a44-150">OUTPUTS</span></span>

### <span data-ttu-id="d2a44-151">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d2a44-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="d2a44-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2a44-152">NOTES</span></span>

## <span data-ttu-id="d2a44-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2a44-153">RELATED LINKS</span></span>

[<span data-ttu-id="d2a44-154">Nowe — AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d2a44-154">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="d2a44-155">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d2a44-155">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="d2a44-156">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="d2a44-156">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


