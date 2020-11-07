---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
ms.openlocfilehash: 38ad6f5631f816070e9d59ba7b78c2a39cff2b2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717142"
---
# <span data-ttu-id="5c5e6-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5c5e6-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="5c5e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5e6-103">Pobiera reguły specyfikacji CORS dla typu usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c5e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c5e6-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c5e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c5e6-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5e6-106">Polecenie cmdlet **Get-AzureStorageCORSRule** pobiera reguły specyfikacji CORS (Cross-Origin Resource Sharing) dla typu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="5c5e6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c5e6-107">EXAMPLES</span></span>

### <span data-ttu-id="5c5e6-108">Przykład 1: pobieranie reguł CORS usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="5c5e6-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="5c5e6-109">To polecenie pobiera reguły CORS dla typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="5c5e6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c5e6-110">PARAMETERS</span></span>

### <span data-ttu-id="5c5e6-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5c5e6-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5c5e6-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5c5e6-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5c5e6-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5c5e6-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5c5e6-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5c5e6-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5c5e6-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5c5e6-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5c5e6-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5c5e6-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5c5e6-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5c5e6-121">-Context</span></span>
<span data-ttu-id="5c5e6-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="5c5e6-123">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5c5e6-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5c5e6-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5c5e6-125">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5c5e6-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5c5e6-126">-ServiceType</span></span>
<span data-ttu-id="5c5e6-127">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet pobiera reguły CORS.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="5c5e6-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5c5e6-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c5e6-129">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="5c5e6-129">Blob</span></span> 
- <span data-ttu-id="5c5e6-130">Tworząc</span><span class="sxs-lookup"><span data-stu-id="5c5e6-130">Table</span></span> 
- <span data-ttu-id="5c5e6-131">Wykonany</span><span class="sxs-lookup"><span data-stu-id="5c5e6-131">Queue</span></span> 
- <span data-ttu-id="5c5e6-132">Plik</span><span class="sxs-lookup"><span data-stu-id="5c5e6-132">File</span></span>

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

### <span data-ttu-id="5c5e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5e6-133">CommonParameters</span></span>
<span data-ttu-id="5c5e6-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5e6-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5e6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5e6-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c5e6-136">INPUTS</span></span>

### <span data-ttu-id="5c5e6-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c5e6-137">IStorageContext</span></span>

<span data-ttu-id="5c5e6-138">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="5c5e6-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="5c5e6-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c5e6-139">OUTPUTS</span></span>

###  
<span data-ttu-id="5c5e6-140">To polecenie cmdlet zwraca tablicę obiektów **PSCORSRule** , które reprezentują reguły specyfikacji CORS obecnie w usłudze.</span><span class="sxs-lookup"><span data-stu-id="5c5e6-140">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="5c5e6-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c5e6-141">NOTES</span></span>

## <span data-ttu-id="5c5e6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c5e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="5c5e6-143">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5c5e6-143">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="5c5e6-144">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5c5e6-144">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


