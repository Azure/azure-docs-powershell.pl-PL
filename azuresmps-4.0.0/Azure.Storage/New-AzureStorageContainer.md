---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523986"
---
# <span data-ttu-id="fbf84-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbf84-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="fbf84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbf84-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf84-103">Tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf84-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="fbf84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbf84-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fbf84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbf84-105">DESCRIPTION</span></span>
<span data-ttu-id="fbf84-106">Polecenie cmdlet **New-AzureStorageContainer** tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf84-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="fbf84-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbf84-107">EXAMPLES</span></span>

### <span data-ttu-id="fbf84-108">Przykład 1. Tworzenie kontenera magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fbf84-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="fbf84-109">To polecenie tworzy kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="fbf84-109">This command creates a storage container.</span></span>

### <span data-ttu-id="fbf84-110">Przykład 2: Tworzenie wielu kontenerów magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fbf84-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="fbf84-111">W tym przykładzie przedstawiono tworzenie wielu kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="fbf84-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="fbf84-112">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="fbf84-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="fbf84-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbf84-113">PARAMETERS</span></span>

### <span data-ttu-id="fbf84-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbf84-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fbf84-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="fbf84-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fbf84-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="fbf84-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fbf84-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="fbf84-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fbf84-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fbf84-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fbf84-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fbf84-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fbf84-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fbf84-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fbf84-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="fbf84-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fbf84-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="fbf84-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fbf84-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="fbf84-123">The default value is 10.</span></span>

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

### <span data-ttu-id="fbf84-124">-Context</span><span class="sxs-lookup"><span data-stu-id="fbf84-124">-Context</span></span>
<span data-ttu-id="fbf84-125">Określa kontekst nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="fbf84-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="fbf84-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbf84-126">-Name</span></span>
<span data-ttu-id="fbf84-127">Określa nazwę nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="fbf84-127">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="fbf84-128">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="fbf84-128">-Permission</span></span>
<span data-ttu-id="fbf84-129">Określa poziom dostępu publicznego do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="fbf84-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="fbf84-130">Domyślnie kontener i wszystkie obiekty blob są dostępne tylko dla właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fbf84-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="fbf84-131">Aby udzielić anonimowym użytkownikom uprawnień do odczytu kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera, aby umożliwić dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="fbf84-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="fbf84-132">Anonimowi użytkownicy mogą czytać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.</span><span class="sxs-lookup"><span data-stu-id="fbf84-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="fbf84-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fbf84-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fbf84-134">Opakowaniu.</span><span class="sxs-lookup"><span data-stu-id="fbf84-134">Container.</span></span>
<span data-ttu-id="fbf84-135">Zapewnia pełny dostęp do odczytu kontenera i jego obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="fbf84-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="fbf84-136">Klienci mogą wyliczyć obiekty blob w kontenerze przez anonimowe żądanie, ale nie można wyliczyć kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="fbf84-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="fbf84-137">Obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="fbf84-137">Blob.</span></span>
<span data-ttu-id="fbf84-138">Zapewnia dostęp do odczytu do danych obiektu BLOB w całym kontenerze za pośrednictwem żądania anonimowego, ale nie umożliwia dostępu do danych kontenera.</span><span class="sxs-lookup"><span data-stu-id="fbf84-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="fbf84-139">Klienci nie mogą wyliczyć obiektów BLOB w kontenerze przy użyciu żądania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="fbf84-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="fbf84-140">Start.</span><span class="sxs-lookup"><span data-stu-id="fbf84-140">Off.</span></span>
<span data-ttu-id="fbf84-141">Które ograniczają dostęp tylko do właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fbf84-141">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="fbf84-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbf84-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fbf84-143">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="fbf84-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fbf84-144">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="fbf84-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fbf84-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf84-145">CommonParameters</span></span>
<span data-ttu-id="fbf84-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf84-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf84-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf84-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf84-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbf84-148">INPUTS</span></span>

## <span data-ttu-id="fbf84-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbf84-149">OUTPUTS</span></span>

## <span data-ttu-id="fbf84-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbf84-150">NOTES</span></span>

## <span data-ttu-id="fbf84-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbf84-151">RELATED LINKS</span></span>

[<span data-ttu-id="fbf84-152">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbf84-152">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="fbf84-153">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbf84-153">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="fbf84-154">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="fbf84-154">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


