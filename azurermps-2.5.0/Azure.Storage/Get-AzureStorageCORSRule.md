---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
ms.openlocfilehash: cf9f4b3a6d58754c4b992163625887afcb3439b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898597"
---
# <span data-ttu-id="90b37-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="90b37-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="90b37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90b37-102">SYNOPSIS</span></span>
<span data-ttu-id="90b37-103">Pobiera reguły specyfikacji CORS dla typu usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="90b37-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90b37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90b37-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="90b37-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90b37-105">DESCRIPTION</span></span>
<span data-ttu-id="90b37-106">Polecenie cmdlet **Get-AzureStorageCORSRule** pobiera reguły specyfikacji CORS (Cross-Origin Resource Sharing) dla typu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="90b37-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="90b37-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90b37-107">EXAMPLES</span></span>

### <span data-ttu-id="90b37-108">Przykład 1: pobieranie reguł CORS usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="90b37-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="90b37-109">To polecenie pobiera reguły CORS dla typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="90b37-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="90b37-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90b37-110">PARAMETERS</span></span>

### <span data-ttu-id="90b37-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90b37-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="90b37-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="90b37-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="90b37-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="90b37-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="90b37-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="90b37-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="90b37-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="90b37-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="90b37-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="90b37-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="90b37-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="90b37-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="90b37-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="90b37-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="90b37-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="90b37-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="90b37-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="90b37-120">The default value is 10.</span></span>

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

### <span data-ttu-id="90b37-121">-Context</span><span class="sxs-lookup"><span data-stu-id="90b37-121">-Context</span></span>
<span data-ttu-id="90b37-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="90b37-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="90b37-123">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="90b37-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="90b37-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b37-124">-DefaultProfile</span></span>
<span data-ttu-id="90b37-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90b37-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90b37-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90b37-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="90b37-127">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="90b37-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="90b37-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="90b37-128">-ServiceType</span></span>
<span data-ttu-id="90b37-129">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet pobiera reguły CORS.</span><span class="sxs-lookup"><span data-stu-id="90b37-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="90b37-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90b37-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90b37-131">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="90b37-131">Blob</span></span> 
- <span data-ttu-id="90b37-132">Tworząc</span><span class="sxs-lookup"><span data-stu-id="90b37-132">Table</span></span> 
- <span data-ttu-id="90b37-133">Wykonany</span><span class="sxs-lookup"><span data-stu-id="90b37-133">Queue</span></span> 
- <span data-ttu-id="90b37-134">Plik</span><span class="sxs-lookup"><span data-stu-id="90b37-134">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b37-135">CommonParameters</span></span>
<span data-ttu-id="90b37-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b37-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b37-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b37-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90b37-138">INPUTS</span></span>

### <span data-ttu-id="90b37-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90b37-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="90b37-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90b37-140">OUTPUTS</span></span>

### <span data-ttu-id="90b37-141">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="90b37-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="90b37-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90b37-142">NOTES</span></span>

## <span data-ttu-id="90b37-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90b37-143">RELATED LINKS</span></span>

[<span data-ttu-id="90b37-144">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="90b37-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="90b37-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="90b37-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


