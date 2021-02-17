---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198442"
---
# <span data-ttu-id="43366-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43366-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="43366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43366-102">SYNOPSIS</span></span>
<span data-ttu-id="43366-103">Tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43366-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="43366-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43366-104">SYNTAX</span></span>

### <span data-ttu-id="43366-105">ContainerName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="43366-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="43366-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="43366-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="43366-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="43366-107">DESCRIPTION</span></span>
<span data-ttu-id="43366-108">Polecenie **cmdlet New-AzStorageContainer** tworzy kontener magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43366-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="43366-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43366-109">EXAMPLES</span></span>

### <span data-ttu-id="43366-110">Przykład 1. Tworzenie kontenera magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="43366-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="43366-111">To polecenie tworzy kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="43366-111">This command creates a storage container.</span></span>

### <span data-ttu-id="43366-112">Przykład 2. Tworzenie wielu kontenerów magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="43366-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="43366-113">W tym przykładzie jest tworzenie wielu kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="43366-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="43366-114">Używa metody **Split** klasy .NET **String,** a następnie przekazuje nazwy w potoku.</span><span class="sxs-lookup"><span data-stu-id="43366-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="43366-115">Przykład 3. Tworzenie kontenera magazynu platformy Azure z zakresem szyfrowania</span><span class="sxs-lookup"><span data-stu-id="43366-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="43366-116">To polecenie tworzy kontener magazynu z domyślnym zakresem szyfrowania jako myencryptscope i wstępnie odwróć przekazywanie obiektów blob z innym zakresem szyfrowania do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="43366-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="43366-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43366-117">PARAMETERS</span></span>

### <span data-ttu-id="43366-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43366-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="43366-119">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="43366-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="43366-120">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="43366-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="43366-121">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="43366-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="43366-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="43366-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="43366-123">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="43366-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="43366-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="43366-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="43366-125">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="43366-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="43366-126">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="43366-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="43366-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="43366-127">The default value is 10.</span></span>

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

### <span data-ttu-id="43366-128">— kontekst</span><span class="sxs-lookup"><span data-stu-id="43366-128">-Context</span></span>
<span data-ttu-id="43366-129">Określa kontekst dla nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="43366-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="43366-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="43366-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="43366-131">Domyślny kontener do stosowania określonego zakresu szyfrowania dla wszystkich zapisów.</span><span class="sxs-lookup"><span data-stu-id="43366-131">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="43366-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43366-132">-DefaultProfile</span></span>
<span data-ttu-id="43366-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43366-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43366-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43366-134">-Name</span></span>
<span data-ttu-id="43366-135">Określa nazwę nowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="43366-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="43366-136">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="43366-136">-Permission</span></span>
<span data-ttu-id="43366-137">Określa poziom publicznego dostępu do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="43366-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="43366-138">Domyślnie kontener i wszystkie obiekty blob w nim uwzględnione mogą być dostępne tylko przez właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="43366-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="43366-139">Aby udzielić użytkownikom anonimowym uprawnień do odczytu kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera w celu włączenia dostępu publicznego.</span><span class="sxs-lookup"><span data-stu-id="43366-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="43366-140">Użytkownicy anonimowi mogą odczytywać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.</span><span class="sxs-lookup"><span data-stu-id="43366-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="43366-141">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="43366-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43366-142">Kontener.</span><span class="sxs-lookup"><span data-stu-id="43366-142">Container.</span></span>
<span data-ttu-id="43366-143">Zapewnia pełny dostęp do odczytu kontenera i jego obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="43366-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="43366-144">Klienci mogą wyliczać obiekty blob w kontenerze za pośrednictwem żądania anonimowego, ale nie mogą wyliczać kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="43366-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="43366-145">Obiekt blob.</span><span class="sxs-lookup"><span data-stu-id="43366-145">Blob.</span></span>
<span data-ttu-id="43366-146">Zapewnia dostęp do odczytu danych obiektów blob w kontenerze za pośrednictwem żądania anonimowego, ale nie zapewnia dostępu do danych kontenera.</span><span class="sxs-lookup"><span data-stu-id="43366-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="43366-147">Klienci nie mogą wyliczać obiektów blob w kontenerze przy użyciu żądania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="43366-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="43366-148">Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="43366-148">Off.</span></span>
<span data-ttu-id="43366-149">Ograniczenie dostępu tylko do właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="43366-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="43366-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="43366-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="43366-151">Blokowanie zastępowania zakresu szyfrowania z domyślnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="43366-151">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="43366-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="43366-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="43366-153">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="43366-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="43366-154">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="43366-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="43366-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43366-155">CommonParameters</span></span>
<span data-ttu-id="43366-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43366-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43366-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43366-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43366-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43366-158">INPUTS</span></span>

### <span data-ttu-id="43366-159">System.String</span><span class="sxs-lookup"><span data-stu-id="43366-159">System.String</span></span>

### <span data-ttu-id="43366-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="43366-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="43366-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43366-161">OUTPUTS</span></span>

### <span data-ttu-id="43366-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43366-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="43366-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43366-163">NOTES</span></span>

## <span data-ttu-id="43366-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43366-164">RELATED LINKS</span></span>

[<span data-ttu-id="43366-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43366-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="43366-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="43366-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="43366-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="43366-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


