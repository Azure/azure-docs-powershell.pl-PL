---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190706"
---
# <span data-ttu-id="131bd-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="131bd-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="131bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="131bd-102">SYNOPSIS</span></span>
<span data-ttu-id="131bd-103">Ustawia uprawnienie dostępu publicznego do kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="131bd-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="131bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="131bd-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="131bd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="131bd-105">DESCRIPTION</span></span>
<span data-ttu-id="131bd-106">Polecenie **cmdlet Set-AzStorageContainerAcl** ustawia uprawnienie dostępu publicznego do określonego kontenera magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="131bd-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="131bd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="131bd-107">EXAMPLES</span></span>

### <span data-ttu-id="131bd-108">Przykład 1. Ustawianie listy ACL magazynu platformy Azure według nazwy</span><span class="sxs-lookup"><span data-stu-id="131bd-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="131bd-109">To polecenie tworzy kontener, który nie ma dostępu publicznego.</span><span class="sxs-lookup"><span data-stu-id="131bd-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="131bd-110">Przykład 2. Ustawianie listy ACL kontenera magazynu platformy Azure przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="131bd-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="131bd-111">To polecenie pobiera wszystkie kontenery magazynu, których nazwa zaczyna się od kontenera, a następnie przekazuje wynik w potoku w celu ustawienia dla nich wszystkich uprawnień dostępu do obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="131bd-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="131bd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="131bd-112">PARAMETERS</span></span>

### <span data-ttu-id="131bd-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="131bd-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="131bd-114">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="131bd-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="131bd-115">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="131bd-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="131bd-116">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="131bd-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="131bd-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="131bd-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="131bd-118">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="131bd-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="131bd-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="131bd-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="131bd-120">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="131bd-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="131bd-121">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="131bd-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="131bd-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="131bd-122">The default value is 10.</span></span>

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

### <span data-ttu-id="131bd-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="131bd-123">-Context</span></span>
<span data-ttu-id="131bd-124">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="131bd-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="131bd-125">Możesz go utworzyć za pomocą polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="131bd-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="131bd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131bd-126">-DefaultProfile</span></span>
<span data-ttu-id="131bd-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="131bd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131bd-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="131bd-128">-Name</span></span>
<span data-ttu-id="131bd-129">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="131bd-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="131bd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="131bd-130">-PassThru</span></span>
<span data-ttu-id="131bd-131">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="131bd-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="131bd-132">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="131bd-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="131bd-133">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="131bd-133">-Permission</span></span>
<span data-ttu-id="131bd-134">Określa poziom publicznego dostępu do tego kontenera.</span><span class="sxs-lookup"><span data-stu-id="131bd-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="131bd-135">Domyślnie kontener i wszystkie obiekty blob w nim uwzględnione mogą być dostępne tylko przez właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="131bd-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="131bd-136">Aby udzielić użytkownikom anonimowym uprawnień do odczytu do kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera w celu włączenia dostępu publicznego.</span><span class="sxs-lookup"><span data-stu-id="131bd-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="131bd-137">Użytkownicy anonimowi mogą odczytywać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.</span><span class="sxs-lookup"><span data-stu-id="131bd-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="131bd-138">Dopuszczalne wartości dla tego parametru to: --Container.</span><span class="sxs-lookup"><span data-stu-id="131bd-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="131bd-139">Zapewnia pełny dostęp do odczytu kontenera i jego obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="131bd-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="131bd-140">Klienci mogą wyliczać obiekty blob w kontenerze za pośrednictwem żądania anonimowego, ale nie mogą wyliczać kontenerów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="131bd-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="131bd-141">—-Blob.</span><span class="sxs-lookup"><span data-stu-id="131bd-141">--Blob.</span></span>
<span data-ttu-id="131bd-142">Zapewnia dostęp do odczytu danych obiektów blob w kontenerze za pośrednictwem żądania anonimowego, ale nie zapewnia dostępu do danych kontenera.</span><span class="sxs-lookup"><span data-stu-id="131bd-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="131bd-143">Klienci nie mogą wyliczać obiektów blob w kontenerze przy użyciu żądania anonimowego.</span><span class="sxs-lookup"><span data-stu-id="131bd-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="131bd-144">—-Wył.</span><span class="sxs-lookup"><span data-stu-id="131bd-144">--Off.</span></span>
<span data-ttu-id="131bd-145">Ogranicza dostęp tylko do właściciela konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="131bd-145">Restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="131bd-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="131bd-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="131bd-147">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="131bd-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="131bd-148">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="131bd-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="131bd-149">Czas po stronie serwera dla każdego żądania jest ubocznym.</span><span class="sxs-lookup"><span data-stu-id="131bd-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="131bd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131bd-150">CommonParameters</span></span>
<span data-ttu-id="131bd-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131bd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131bd-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="131bd-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131bd-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="131bd-153">INPUTS</span></span>

### <span data-ttu-id="131bd-154">System.String</span><span class="sxs-lookup"><span data-stu-id="131bd-154">System.String</span></span>

### <span data-ttu-id="131bd-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="131bd-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="131bd-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="131bd-156">OUTPUTS</span></span>

### <span data-ttu-id="131bd-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="131bd-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="131bd-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="131bd-158">NOTES</span></span>

## <span data-ttu-id="131bd-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="131bd-159">RELATED LINKS</span></span>

[<span data-ttu-id="131bd-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="131bd-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="131bd-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="131bd-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="131bd-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="131bd-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


