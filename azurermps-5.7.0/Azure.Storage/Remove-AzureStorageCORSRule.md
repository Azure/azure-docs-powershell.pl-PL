---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
ms.openlocfilehash: 873cee6ce1f724fb925ae743133ecfb9a1a5210a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542767"
---
# <span data-ttu-id="ba324-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ba324-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="ba324-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba324-102">SYNOPSIS</span></span>
<span data-ttu-id="ba324-103">Usuwa składnik CORS dla usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="ba324-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba324-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba324-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba324-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba324-105">DESCRIPTION</span></span>
<span data-ttu-id="ba324-106">Polecenie cmdlet **Remove-AzureStorageCORSRule** usuwa udostępnianie zasobów Cross-Origin (CORS) dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ba324-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="ba324-107">To polecenie cmdlet usuwa wszystkie reguły CORS w typie usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="ba324-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="ba324-108">Typy usług magazynowania dla tego polecenia cmdlet to obiekt BLOB, tabela, kolejka i plik.</span><span class="sxs-lookup"><span data-stu-id="ba324-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="ba324-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba324-109">EXAMPLES</span></span>

### <span data-ttu-id="ba324-110">Przykład 1: usuwanie reguł CORS dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="ba324-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="ba324-111">To polecenie usuwa reguły CORS dla typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="ba324-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="ba324-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba324-112">PARAMETERS</span></span>

### <span data-ttu-id="ba324-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ba324-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ba324-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="ba324-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ba324-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="ba324-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ba324-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="ba324-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ba324-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ba324-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ba324-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ba324-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ba324-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ba324-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ba324-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="ba324-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ba324-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="ba324-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ba324-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="ba324-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ba324-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ba324-123">-Context</span></span>
<span data-ttu-id="ba324-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ba324-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ba324-125">Aby uzyskać kontekst miejsca do magazynowania, New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba324-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ba324-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ba324-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ba324-127">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="ba324-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ba324-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ba324-128">-ServiceType</span></span>
<span data-ttu-id="ba324-129">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet usuwa reguły.</span><span class="sxs-lookup"><span data-stu-id="ba324-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="ba324-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ba324-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba324-131">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="ba324-131">Blob</span></span> 
- <span data-ttu-id="ba324-132">Tworząc</span><span class="sxs-lookup"><span data-stu-id="ba324-132">Table</span></span> 
- <span data-ttu-id="ba324-133">Wykonany</span><span class="sxs-lookup"><span data-stu-id="ba324-133">Queue</span></span> 
- <span data-ttu-id="ba324-134">Plik</span><span class="sxs-lookup"><span data-stu-id="ba324-134">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba324-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba324-135">CommonParameters</span></span>
<span data-ttu-id="ba324-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba324-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba324-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba324-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba324-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba324-138">INPUTS</span></span>

### <span data-ttu-id="ba324-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ba324-139">IStorageContext</span></span>

<span data-ttu-id="ba324-140">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="ba324-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ba324-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba324-141">OUTPUTS</span></span>

## <span data-ttu-id="ba324-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba324-142">NOTES</span></span>

## <span data-ttu-id="ba324-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba324-143">RELATED LINKS</span></span>

[<span data-ttu-id="ba324-144">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ba324-144">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="ba324-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ba324-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)

