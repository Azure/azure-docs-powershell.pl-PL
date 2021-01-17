---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374017"
---
# <span data-ttu-id="537a6-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="537a6-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="537a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="537a6-102">SYNOPSIS</span></span>
<span data-ttu-id="537a6-103">Tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="537a6-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="537a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="537a6-104">SYNTAX</span></span>

### <span data-ttu-id="537a6-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="537a6-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="537a6-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="537a6-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="537a6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="537a6-107">DESCRIPTION</span></span>
<span data-ttu-id="537a6-108">Polecenie cmdlet **New-AzStorageContainer** tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="537a6-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="537a6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="537a6-109">EXAMPLES</span></span>

### <span data-ttu-id="537a6-110">Przykład 1. Tworzenie kontenera magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="537a6-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="537a6-111">To polecenie tworzy kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="537a6-111">This command creates a storage container.</span></span>

### <span data-ttu-id="537a6-112">Przykład 2: Tworzenie wielu kontenerów magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="537a6-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="537a6-113">W tym przykładzie przedstawiono tworzenie wielu kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="537a6-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="537a6-114">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="537a6-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="537a6-115">Przykład 3: Tworzenie kontenera magazynu platformy Azure z zakresem szyfrowania</span><span class="sxs-lookup"><span data-stu-id="537a6-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="537a6-116">To polecenie tworzy kontener magazynu z domyślnym zakresem szyfrowania, który jest myencryptscope i przekazano do tego kontenera przekazanie obiektu BLOB z innym zakresem szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="537a6-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="537a6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="537a6-117">PARAMETERS</span></span>

### <span data-ttu-id="537a6-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="537a6-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="537a6-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="537a6-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="537a6-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="537a6-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="537a6-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="537a6-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="537a6-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="537a6-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="537a6-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="537a6-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="537a6-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="537a6-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="537a6-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="537a6-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="537a6-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="537a6-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="537a6-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="537a6-127">The default value is 10.</span></span>

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

### <span data-ttu-id="537a6-128">-Context</span><span class="sxs-lookup"><span data-stu-id="537a6-128">-Context</span></span>
<span data-ttu-id="537a6-129">Określa kontekst nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="537a6-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="537a6-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="537a6-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="537a6-131">Domyślnie kontener używający określonego zakresu szyfrowania dla wszystkich zapisów.</span><span class="sxs-lookup"><span data-stu-id="537a6-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537a6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537a6-132">-DefaultProfile</span></span>
<span data-ttu-id="537a6-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="537a6-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="537a6-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="537a6-134">-Name</span></span>
<span data-ttu-id="537a6-135">Określa nazwę nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="537a6-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="537a6-136">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="537a6-136">-Permission</span></span>
<span data-ttu-id="537a6-137">Określa poziom dostępu publicznego do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="537a6-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="537a6-138">Domyślnie kontener i wszystkie obiekty blob są dostępne tylko dla właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="537a6-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="537a6-139">Aby udzielić anonimowym użytkownikom uprawnień do odczytu kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera, aby umożliwić dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="537a6-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="537a6-140">Anonimowi użytkownicy mogą czytać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.</span><span class="sxs-lookup"><span data-stu-id="537a6-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="537a6-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="537a6-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="537a6-142">Opakowaniu.</span><span class="sxs-lookup"><span data-stu-id="537a6-142">Container.</span></span>
<span data-ttu-id="537a6-143">Zapewnia pełny dostęp do odczytu kontenera i jego obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="537a6-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="537a6-144">Klienci mogą wyliczyć obiekty blob w kontenerze przez anonimowe żądanie, ale nie można wyliczyć kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="537a6-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="537a6-145">Obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="537a6-145">Blob.</span></span>
<span data-ttu-id="537a6-146">Zapewnia dostęp do odczytu do danych obiektu BLOB w całym kontenerze za pośrednictwem żądania anonimowego, ale nie umożliwia dostępu do danych kontenera.</span><span class="sxs-lookup"><span data-stu-id="537a6-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="537a6-147">Klienci nie mogą wyliczyć obiektów BLOB w kontenerze przy użyciu żądania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="537a6-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="537a6-148">Start.</span><span class="sxs-lookup"><span data-stu-id="537a6-148">Off.</span></span>
<span data-ttu-id="537a6-149">Które ograniczają dostęp tylko do właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="537a6-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="537a6-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="537a6-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="537a6-151">Blokowanie przesłonięcia zakresu szyfrowania z domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="537a6-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537a6-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="537a6-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="537a6-153">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="537a6-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="537a6-154">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="537a6-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="537a6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537a6-155">CommonParameters</span></span>
<span data-ttu-id="537a6-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="537a6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537a6-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="537a6-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537a6-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="537a6-158">INPUTS</span></span>

### <span data-ttu-id="537a6-159">System. String</span><span class="sxs-lookup"><span data-stu-id="537a6-159">System.String</span></span>

### <span data-ttu-id="537a6-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="537a6-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="537a6-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="537a6-161">OUTPUTS</span></span>

### <span data-ttu-id="537a6-162">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="537a6-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="537a6-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="537a6-163">NOTES</span></span>

## <span data-ttu-id="537a6-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="537a6-164">RELATED LINKS</span></span>

[<span data-ttu-id="537a6-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="537a6-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="537a6-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="537a6-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="537a6-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="537a6-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


