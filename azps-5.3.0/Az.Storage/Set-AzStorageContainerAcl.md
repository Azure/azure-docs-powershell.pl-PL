---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376154"
---
# <span data-ttu-id="d1962-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="d1962-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="d1962-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1962-102">SYNOPSIS</span></span>
<span data-ttu-id="d1962-103">Ustawia uprawnienie dostępu publicznego do kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="d1962-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="d1962-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1962-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d1962-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d1962-105">DESCRIPTION</span></span>
<span data-ttu-id="d1962-106">Polecenie cmdlet **Set-AzStorageContainerAcl** ustawia uprawnienie dostępu publicznego do określonego kontenera magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d1962-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="d1962-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1962-107">EXAMPLES</span></span>

### <span data-ttu-id="d1962-108">Przykład 1: ustawianie listy ACL kontenera magazynu platformy Azure według nazwy</span><span class="sxs-lookup"><span data-stu-id="d1962-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="d1962-109">To polecenie tworzy kontener bez dostępu publicznego.</span><span class="sxs-lookup"><span data-stu-id="d1962-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="d1962-110">Przykład 2: ustawianie listy ACL kontenera magazynu platformy Azure przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="d1962-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="d1962-111">To polecenie pobiera wszystkie kontenery magazynu, których nazwa zaczyna się od kontenera, a następnie przekazuje wynik w potoku, aby ustawić dla niego uprawnienie dostępu do obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="d1962-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="d1962-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1962-112">PARAMETERS</span></span>

### <span data-ttu-id="d1962-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1962-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d1962-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="d1962-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d1962-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="d1962-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d1962-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="d1962-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d1962-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d1962-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d1962-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="d1962-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d1962-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="d1962-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d1962-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="d1962-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d1962-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="d1962-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d1962-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="d1962-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d1962-123">-Context</span><span class="sxs-lookup"><span data-stu-id="d1962-123">-Context</span></span>
<span data-ttu-id="d1962-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d1962-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d1962-125">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d1962-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d1962-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1962-126">-DefaultProfile</span></span>
<span data-ttu-id="d1962-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1962-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1962-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1962-128">-Name</span></span>
<span data-ttu-id="d1962-129">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="d1962-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="d1962-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1962-130">-PassThru</span></span>
<span data-ttu-id="d1962-131">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d1962-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d1962-132">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d1962-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1962-133">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="d1962-133">-Permission</span></span>
<span data-ttu-id="d1962-134">Określa poziom dostępu publicznego do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d1962-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="d1962-135">Domyślnie kontener i wszystkie obiekty blob są dostępne tylko dla właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d1962-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="d1962-136">Aby udzielić anonimowym użytkownikom uprawnień do odczytu kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera, aby umożliwić dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="d1962-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="d1962-137">Anonimowi użytkownicy mogą czytać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.</span><span class="sxs-lookup"><span data-stu-id="d1962-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="d1962-138">Dopuszczalne wartości tego parametru to:--kontener.</span><span class="sxs-lookup"><span data-stu-id="d1962-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="d1962-139">Zapewnia pełny dostęp do odczytu kontenera i jego obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="d1962-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="d1962-140">Klienci mogą wyliczyć obiekty blob w kontenerze przez anonimowe żądanie, ale nie można wyliczyć kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="d1962-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="d1962-141">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="d1962-141">--Blob.</span></span>
<span data-ttu-id="d1962-142">Zapewnia dostęp do odczytu do danych obiektu BLOB w kontenerze za pośrednictwem żądania anonimowego, ale nie umożliwia dostępu do danych kontenera.</span><span class="sxs-lookup"><span data-stu-id="d1962-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="d1962-143">Klienci nie mogą wyliczyć obiektów BLOB w kontenerze przy użyciu żądania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="d1962-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="d1962-144">--Wył.</span><span class="sxs-lookup"><span data-stu-id="d1962-144">--Off.</span></span>
<span data-ttu-id="d1962-145">Ogranicza dostęp tylko do właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d1962-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1962-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1962-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d1962-147">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="d1962-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d1962-148">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="d1962-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="d1962-149">Limit czasu po stronie serwera dla każdego żądania.</span><span class="sxs-lookup"><span data-stu-id="d1962-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="d1962-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1962-150">CommonParameters</span></span>
<span data-ttu-id="d1962-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1962-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1962-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1962-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1962-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1962-153">INPUTS</span></span>

### <span data-ttu-id="d1962-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d1962-154">System.String</span></span>

### <span data-ttu-id="d1962-155">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1962-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1962-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1962-156">OUTPUTS</span></span>

### <span data-ttu-id="d1962-157">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d1962-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="d1962-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1962-158">NOTES</span></span>

## <span data-ttu-id="d1962-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1962-159">RELATED LINKS</span></span>

[<span data-ttu-id="d1962-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d1962-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="d1962-161">Nowe — AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d1962-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="d1962-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d1962-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


