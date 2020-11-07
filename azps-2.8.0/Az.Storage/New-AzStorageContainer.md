---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: c4e3ba53ccb583b72001bfdfcc08c15025eda0da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888105"
---
# <span data-ttu-id="48d7c-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="48d7c-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="48d7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="48d7c-103">Tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48d7c-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="48d7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48d7c-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="48d7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48d7c-105">DESCRIPTION</span></span>
<span data-ttu-id="48d7c-106">Polecenie cmdlet **New-AzStorageContainer** tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48d7c-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="48d7c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48d7c-107">EXAMPLES</span></span>

### <span data-ttu-id="48d7c-108">Przykład 1. Tworzenie kontenera magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="48d7c-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="48d7c-109">To polecenie tworzy kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="48d7c-109">This command creates a storage container.</span></span>

### <span data-ttu-id="48d7c-110">Przykład 2: Tworzenie wielu kontenerów magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="48d7c-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="48d7c-111">W tym przykładzie przedstawiono tworzenie wielu kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="48d7c-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="48d7c-112">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="48d7c-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="48d7c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48d7c-113">PARAMETERS</span></span>

### <span data-ttu-id="48d7c-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="48d7c-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="48d7c-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="48d7c-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="48d7c-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="48d7c-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="48d7c-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="48d7c-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="48d7c-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="48d7c-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="48d7c-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="48d7c-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="48d7c-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="48d7c-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="48d7c-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="48d7c-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="48d7c-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="48d7c-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="48d7c-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="48d7c-123">The default value is 10.</span></span>

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

### <span data-ttu-id="48d7c-124">-Context</span><span class="sxs-lookup"><span data-stu-id="48d7c-124">-Context</span></span>
<span data-ttu-id="48d7c-125">Określa kontekst nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="48d7c-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="48d7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d7c-126">-DefaultProfile</span></span>
<span data-ttu-id="48d7c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48d7c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d7c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48d7c-128">-Name</span></span>
<span data-ttu-id="48d7c-129">Określa nazwę nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="48d7c-129">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48d7c-130">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="48d7c-130">-Permission</span></span>
<span data-ttu-id="48d7c-131">Określa poziom dostępu publicznego do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="48d7c-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="48d7c-132">Domyślnie kontener i wszystkie obiekty blob są dostępne tylko dla właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="48d7c-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="48d7c-133">Aby udzielić anonimowym użytkownikom uprawnień do odczytu kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera, aby umożliwić dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="48d7c-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="48d7c-134">Anonimowi użytkownicy mogą czytać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.</span><span class="sxs-lookup"><span data-stu-id="48d7c-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="48d7c-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="48d7c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48d7c-136">Opakowaniu.</span><span class="sxs-lookup"><span data-stu-id="48d7c-136">Container.</span></span>
<span data-ttu-id="48d7c-137">Zapewnia pełny dostęp do odczytu kontenera i jego obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="48d7c-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="48d7c-138">Klienci mogą wyliczyć obiekty blob w kontenerze przez anonimowe żądanie, ale nie można wyliczyć kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="48d7c-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="48d7c-139">Obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="48d7c-139">Blob.</span></span>
<span data-ttu-id="48d7c-140">Zapewnia dostęp do odczytu do danych obiektu BLOB w całym kontenerze za pośrednictwem żądania anonimowego, ale nie umożliwia dostępu do danych kontenera.</span><span class="sxs-lookup"><span data-stu-id="48d7c-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="48d7c-141">Klienci nie mogą wyliczyć obiektów BLOB w kontenerze przy użyciu żądania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="48d7c-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="48d7c-142">Start.</span><span class="sxs-lookup"><span data-stu-id="48d7c-142">Off.</span></span>
<span data-ttu-id="48d7c-143">Które ograniczają dostęp tylko do właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="48d7c-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d7c-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="48d7c-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="48d7c-145">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="48d7c-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="48d7c-146">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="48d7c-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="48d7c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d7c-147">CommonParameters</span></span>
<span data-ttu-id="48d7c-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d7c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d7c-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d7c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d7c-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48d7c-150">INPUTS</span></span>

### <span data-ttu-id="48d7c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="48d7c-151">System.String</span></span>

### <span data-ttu-id="48d7c-152">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="48d7c-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="48d7c-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48d7c-153">OUTPUTS</span></span>

### <span data-ttu-id="48d7c-154">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="48d7c-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="48d7c-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48d7c-155">NOTES</span></span>

## <span data-ttu-id="48d7c-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48d7c-156">RELATED LINKS</span></span>

[<span data-ttu-id="48d7c-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="48d7c-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="48d7c-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="48d7c-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="48d7c-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="48d7c-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


