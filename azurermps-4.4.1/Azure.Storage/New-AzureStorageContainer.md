---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 7e7672368a2f9e102e1e073c1f10be609e658cfa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525845"
---
# <span data-ttu-id="db2ac-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db2ac-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="db2ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="db2ac-103">Tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="db2ac-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db2ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db2ac-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="db2ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="db2ac-106">Polecenie cmdlet **New-AzureStorageContainer** tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="db2ac-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="db2ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db2ac-107">EXAMPLES</span></span>

### <span data-ttu-id="db2ac-108">Przykład 1. Tworzenie kontenera magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="db2ac-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="db2ac-109">To polecenie tworzy kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="db2ac-109">This command creates a storage container.</span></span>

### <span data-ttu-id="db2ac-110">Przykład 2: Tworzenie wielu kontenerów magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="db2ac-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="db2ac-111">W tym przykładzie przedstawiono tworzenie wielu kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="db2ac-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="db2ac-112">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="db2ac-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="db2ac-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db2ac-113">PARAMETERS</span></span>

### <span data-ttu-id="db2ac-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="db2ac-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="db2ac-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="db2ac-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="db2ac-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="db2ac-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="db2ac-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="db2ac-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="db2ac-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="db2ac-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="db2ac-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="db2ac-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="db2ac-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="db2ac-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="db2ac-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="db2ac-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="db2ac-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="db2ac-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="db2ac-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="db2ac-123">The default value is 10.</span></span>

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

### <span data-ttu-id="db2ac-124">-Context</span><span class="sxs-lookup"><span data-stu-id="db2ac-124">-Context</span></span>
<span data-ttu-id="db2ac-125">Określa kontekst nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="db2ac-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="db2ac-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db2ac-126">-Name</span></span>
<span data-ttu-id="db2ac-127">Określa nazwę nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="db2ac-127">Specifies a name for the new container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db2ac-128">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="db2ac-128">-Permission</span></span>
<span data-ttu-id="db2ac-129">Określa poziom dostępu publicznego do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="db2ac-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="db2ac-130">Domyślnie kontener i wszystkie obiekty blob są dostępne tylko dla właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="db2ac-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="db2ac-131">Aby udzielić anonimowym użytkownikom uprawnień do odczytu kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera, aby umożliwić dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="db2ac-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="db2ac-132">Anonimowi użytkownicy mogą czytać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.</span><span class="sxs-lookup"><span data-stu-id="db2ac-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="db2ac-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="db2ac-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db2ac-134">Opakowaniu.</span><span class="sxs-lookup"><span data-stu-id="db2ac-134">Container.</span></span>
<span data-ttu-id="db2ac-135">Zapewnia pełny dostęp do odczytu kontenera i jego obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="db2ac-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="db2ac-136">Klienci mogą wyliczyć obiekty blob w kontenerze przez anonimowe żądanie, ale nie można wyliczyć kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="db2ac-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="db2ac-137">Obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="db2ac-137">Blob.</span></span>
<span data-ttu-id="db2ac-138">Zapewnia dostęp do odczytu do danych obiektu BLOB w całym kontenerze za pośrednictwem żądania anonimowego, ale nie umożliwia dostępu do danych kontenera.</span><span class="sxs-lookup"><span data-stu-id="db2ac-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="db2ac-139">Klienci nie mogą wyliczyć obiektów BLOB w kontenerze przy użyciu żądania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="db2ac-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="db2ac-140">Start.</span><span class="sxs-lookup"><span data-stu-id="db2ac-140">Off.</span></span>
<span data-ttu-id="db2ac-141">Które ograniczają dostęp tylko do właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="db2ac-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2ac-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="db2ac-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="db2ac-143">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="db2ac-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="db2ac-144">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="db2ac-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="db2ac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2ac-145">CommonParameters</span></span>
<span data-ttu-id="db2ac-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2ac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2ac-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2ac-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2ac-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db2ac-148">INPUTS</span></span>

### <span data-ttu-id="db2ac-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="db2ac-149">IStorageContext</span></span>

<span data-ttu-id="db2ac-150">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="db2ac-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="db2ac-151">Ciąg</span><span class="sxs-lookup"><span data-stu-id="db2ac-151">String</span></span>

<span data-ttu-id="db2ac-152">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="db2ac-152">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="db2ac-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db2ac-153">OUTPUTS</span></span>

### <span data-ttu-id="db2ac-154">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db2ac-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="db2ac-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db2ac-155">NOTES</span></span>

## <span data-ttu-id="db2ac-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db2ac-156">RELATED LINKS</span></span>

[<span data-ttu-id="db2ac-157">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db2ac-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="db2ac-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db2ac-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="db2ac-159">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="db2ac-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


