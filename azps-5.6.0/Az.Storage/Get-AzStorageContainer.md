---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 15aefebea30e829371c57c3c1cd575a604b81eaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981530"
---
# <span data-ttu-id="b05dc-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b05dc-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="b05dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b05dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b05dc-103">Wyświetla listę kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="b05dc-103">Lists the storage containers.</span></span>

## <span data-ttu-id="b05dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b05dc-104">SYNTAX</span></span>

### <span data-ttu-id="b05dc-105">ContainerName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b05dc-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b05dc-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="b05dc-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b05dc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b05dc-107">DESCRIPTION</span></span>
<span data-ttu-id="b05dc-108">Polecenie **cmdlet Get-AzStorageContainer** wyświetla listę kontenerów magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b05dc-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="b05dc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b05dc-109">EXAMPLES</span></span>

### <span data-ttu-id="b05dc-110">Przykład 1. Uzyskiwanie obiektu blob magazynu platformy Azure według nazwy</span><span class="sxs-lookup"><span data-stu-id="b05dc-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="b05dc-111">W tym przykładzie do zwrócenia listy wszystkich kontenerów o nazwie, która zaczyna się od kontenera, jest używany symbol wieloznaczny.</span><span class="sxs-lookup"><span data-stu-id="b05dc-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="b05dc-112">Przykład 2. Pobierz kontener magazynu platformy Azure według prefiksu nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="b05dc-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="b05dc-113">W tym przykładzie *użyto parametru Prefix* w celu zwrócenia listy wszystkich kontenerów o nazwie, która rozpoczyna się od kontenera.</span><span class="sxs-lookup"><span data-stu-id="b05dc-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="b05dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b05dc-114">PARAMETERS</span></span>

### <span data-ttu-id="b05dc-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b05dc-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b05dc-116">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b05dc-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b05dc-117">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="b05dc-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b05dc-118">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="b05dc-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b05dc-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b05dc-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b05dc-120">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b05dc-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b05dc-121">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b05dc-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b05dc-122">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="b05dc-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b05dc-123">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b05dc-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b05dc-124">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b05dc-124">The default value is 10.</span></span>

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

### <span data-ttu-id="b05dc-125">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b05dc-125">-Context</span></span>
<span data-ttu-id="b05dc-126">Określa kontekst magazynowania.</span><span class="sxs-lookup"><span data-stu-id="b05dc-126">Specifies the storage context.</span></span>
<span data-ttu-id="b05dc-127">Aby go utworzyć, możesz użyć New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b05dc-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="b05dc-128">Uprawnienia kontenera nie zostaną pobrane w przypadku użycia kontekstu magazynu utworzonego za pomocą tokenu SAS, ponieważ uprawnienia kontenera zapytań wymagają uprawnień klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b05dc-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="b05dc-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b05dc-129">-ContinuationToken</span></span>
<span data-ttu-id="b05dc-130">Określa token kontynuacji dla listy obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="b05dc-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05dc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05dc-131">-DefaultProfile</span></span>
<span data-ttu-id="b05dc-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b05dc-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b05dc-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b05dc-133">-MaxCount</span></span>
<span data-ttu-id="b05dc-134">Określa maksymalną liczbę obiektów zwracanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b05dc-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="b05dc-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b05dc-135">-Name</span></span>
<span data-ttu-id="b05dc-136">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="b05dc-136">Specifies the container name.</span></span>
<span data-ttu-id="b05dc-137">Jeśli nazwa kontenera jest pusta, polecenie cmdlet wyświetla listę wszystkich kontenerów.</span><span class="sxs-lookup"><span data-stu-id="b05dc-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="b05dc-138">W przeciwnym razie wyświetla listę wszystkich kontenerów, które pasują do określonej nazwy lub zwykłego wzorca nazw.</span><span class="sxs-lookup"><span data-stu-id="b05dc-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b05dc-139">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="b05dc-139">-Prefix</span></span>
<span data-ttu-id="b05dc-140">Określa prefiks używany w nazwie kontenera lub kontenerów, które mają zostać użyte.</span><span class="sxs-lookup"><span data-stu-id="b05dc-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="b05dc-141">Dzięki temu można znaleźć wszystkie kontenery, które zaczynają się od tego samego ciągu znaków, na przykład "my" lub "test".</span><span class="sxs-lookup"><span data-stu-id="b05dc-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05dc-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b05dc-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b05dc-143">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="b05dc-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b05dc-144">Jeśli określony interwał pominie się przed rozpoczęciem przetwarzania żądania przez usługę magazynu, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="b05dc-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b05dc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05dc-145">CommonParameters</span></span>
<span data-ttu-id="b05dc-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05dc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05dc-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05dc-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05dc-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b05dc-148">INPUTS</span></span>

### <span data-ttu-id="b05dc-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b05dc-149">System.String</span></span>

### <span data-ttu-id="b05dc-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b05dc-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b05dc-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b05dc-151">OUTPUTS</span></span>

### <span data-ttu-id="b05dc-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b05dc-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="b05dc-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b05dc-153">NOTES</span></span>

## <span data-ttu-id="b05dc-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b05dc-154">RELATED LINKS</span></span>

[<span data-ttu-id="b05dc-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b05dc-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="b05dc-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b05dc-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="b05dc-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="b05dc-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


