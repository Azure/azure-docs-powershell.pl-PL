---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 19dbbe53347a06030c175f45f722bfd287863d85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545936"
---
# <span data-ttu-id="ec173-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ec173-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="ec173-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec173-102">SYNOPSIS</span></span>
<span data-ttu-id="ec173-103">Pobiera zasady programu Access lub zasady dotyczące kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ec173-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec173-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec173-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ec173-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec173-105">DESCRIPTION</span></span>
<span data-ttu-id="ec173-106">Polecenie cmdlet **Get-AzureStorageContainerStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dotyczących kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ec173-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ec173-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec173-107">EXAMPLES</span></span>

### <span data-ttu-id="ec173-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="ec173-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="ec173-109">To polecenie pobiera zasady dostępu o nazwie Policy22 w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="ec173-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="ec173-110">Przykład 2: uzyskiwanie wszystkich przechowywanych zasad dostępu w kontenerze magazynu</span><span class="sxs-lookup"><span data-stu-id="ec173-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="ec173-111">To polecenie pobiera wszystkie zasady dostępu w kontenerze magazynu o nazwie Container07.</span><span class="sxs-lookup"><span data-stu-id="ec173-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="ec173-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec173-112">PARAMETERS</span></span>

### <span data-ttu-id="ec173-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec173-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ec173-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="ec173-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ec173-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="ec173-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ec173-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="ec173-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ec173-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ec173-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ec173-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ec173-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ec173-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ec173-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ec173-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="ec173-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ec173-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="ec173-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ec173-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="ec173-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ec173-123">-Kontener</span><span class="sxs-lookup"><span data-stu-id="ec173-123">-Container</span></span>
<span data-ttu-id="ec173-124">Określa nazwę kontenera usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ec173-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec173-125">-Context</span><span class="sxs-lookup"><span data-stu-id="ec173-125">-Context</span></span>
<span data-ttu-id="ec173-126">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ec173-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="ec173-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="ec173-127">-Policy</span></span>
<span data-ttu-id="ec173-128">Określa zasady dostępu przechowywane na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ec173-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec173-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec173-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ec173-130">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="ec173-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ec173-131">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="ec173-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ec173-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec173-132">CommonParameters</span></span>
<span data-ttu-id="ec173-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec173-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec173-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec173-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec173-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec173-135">INPUTS</span></span>

### <span data-ttu-id="ec173-136">Ciąg</span><span class="sxs-lookup"><span data-stu-id="ec173-136">String</span></span>

<span data-ttu-id="ec173-137">Parametr "Container" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="ec173-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ec173-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec173-138">IStorageContext</span></span>

<span data-ttu-id="ec173-139">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="ec173-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ec173-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec173-140">OUTPUTS</span></span>

### <span data-ttu-id="ec173-141">Microsoft. platformy windowsazure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="ec173-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="ec173-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec173-142">NOTES</span></span>

## <span data-ttu-id="ec173-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec173-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec173-144">Nowe — AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ec173-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ec173-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ec173-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ec173-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ec173-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)

