---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
ms.openlocfilehash: ebcab0d664ee87d94e2affdae0f16556443a97f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524774"
---
# <span data-ttu-id="c624f-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c624f-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="c624f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c624f-102">SYNOPSIS</span></span>
<span data-ttu-id="c624f-103">Zawiera listę kontenerów magazynu.</span><span class="sxs-lookup"><span data-stu-id="c624f-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c624f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c624f-104">SYNTAX</span></span>

### <span data-ttu-id="c624f-105">ContainerName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c624f-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c624f-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="c624f-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c624f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c624f-107">DESCRIPTION</span></span>
<span data-ttu-id="c624f-108">Polecenie cmdlet **Get-AzureStorageContainer** zawiera listę kontenerów magazynu skojarzonych z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c624f-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="c624f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c624f-109">EXAMPLES</span></span>

### <span data-ttu-id="c624f-110">Przykład 1: Pobieranie obiektu blob magazynu platformy Azure według nazwy</span><span class="sxs-lookup"><span data-stu-id="c624f-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="c624f-111">W tym przykładzie użyto symbolu wieloznacznego w celu zwrócenia listy wszystkich kontenerów o nazwie rozpoczynającej się od kontenera.</span><span class="sxs-lookup"><span data-stu-id="c624f-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="c624f-112">Przykład 2: uzyskiwanie prefiksu nazwy kontenera usługi Azure Storage kontener</span><span class="sxs-lookup"><span data-stu-id="c624f-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="c624f-113">W tym przykładzie użyto parametru *prefix* w celu zwrócenia listy wszystkich kontenerów o nazwie rozpoczynającej się od kontenera.</span><span class="sxs-lookup"><span data-stu-id="c624f-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="c624f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c624f-114">PARAMETERS</span></span>

### <span data-ttu-id="c624f-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c624f-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c624f-116">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c624f-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c624f-117">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c624f-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c624f-118">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c624f-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c624f-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c624f-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c624f-120">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c624f-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c624f-121">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c624f-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c624f-122">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="c624f-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c624f-123">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c624f-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c624f-124">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c624f-124">The default value is 10.</span></span>

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

### <span data-ttu-id="c624f-125">-Context</span><span class="sxs-lookup"><span data-stu-id="c624f-125">-Context</span></span>
<span data-ttu-id="c624f-126">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c624f-126">Specifies the storage context.</span></span>
<span data-ttu-id="c624f-127">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c624f-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="c624f-128">Uprawnienia kontenera nie zostaną pobrane, gdy użyjesz kontekstu magazynu utworzonego na podstawie tokenu SAS, ponieważ uprawnienia kontenera kwerendy wymagają uprawnień klucza konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c624f-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="c624f-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="c624f-129">-ContinuationToken</span></span>
<span data-ttu-id="c624f-130">Określa token kontynuacji listy obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="c624f-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c624f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c624f-131">-DefaultProfile</span></span>
<span data-ttu-id="c624f-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c624f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c624f-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c624f-133">-MaxCount</span></span>
<span data-ttu-id="c624f-134">Określa maksymalną liczbę obiektów, które zostanie zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c624f-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="c624f-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c624f-135">-Name</span></span>
<span data-ttu-id="c624f-136">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="c624f-136">Specifies the container name.</span></span>
<span data-ttu-id="c624f-137">Jeśli nazwa kontenera jest pusta, polecenie cmdlet wyświetla wszystkie kontenery.</span><span class="sxs-lookup"><span data-stu-id="c624f-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="c624f-138">W przeciwnym razie wyświetla wszystkie kontenery zgodne z określoną nazwą lub wzorcem zwykłej nazwy.</span><span class="sxs-lookup"><span data-stu-id="c624f-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="c624f-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="c624f-139">-Prefix</span></span>
<span data-ttu-id="c624f-140">Określa prefiks stosowany w nazwie kontenera lub kontenerów, które mają zostać przeszukane.</span><span class="sxs-lookup"><span data-stu-id="c624f-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="c624f-141">Za pomocą tej pozycji można znaleźć wszystkie kontenery, które zaczynają się od tego samego ciągu, na przykład "my" lub "test".</span><span class="sxs-lookup"><span data-stu-id="c624f-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="c624f-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c624f-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c624f-143">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="c624f-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c624f-144">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="c624f-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c624f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c624f-145">CommonParameters</span></span>
<span data-ttu-id="c624f-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c624f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c624f-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c624f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c624f-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c624f-148">INPUTS</span></span>

### <span data-ttu-id="c624f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c624f-149">System.String</span></span>

### <span data-ttu-id="c624f-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c624f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c624f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c624f-151">OUTPUTS</span></span>

### <span data-ttu-id="c624f-152">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c624f-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="c624f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c624f-153">NOTES</span></span>

## <span data-ttu-id="c624f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c624f-154">RELATED LINKS</span></span>

[<span data-ttu-id="c624f-155">Nowe — AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c624f-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="c624f-156">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c624f-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="c624f-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c624f-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


