---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: 4781e5afc5fc560fdfb60dd06b412f4dad9a54cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888145"
---
# <span data-ttu-id="3ca6c-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="3ca6c-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="3ca6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ca6c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca6c-103">Usuwa składnik CORS dla usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="3ca6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ca6c-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3ca6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3ca6c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ca6c-106">Polecenie cmdlet **Remove-AzStorageCORSRule** usuwa udostępnianie zasobów Cross-Origin (CORS) dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="3ca6c-107">To polecenie cmdlet usuwa wszystkie reguły CORS w typie usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="3ca6c-108">Typy usług magazynowania dla tego polecenia cmdlet to obiekt BLOB, tabela, kolejka i plik.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="3ca6c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ca6c-109">EXAMPLES</span></span>

### <span data-ttu-id="3ca6c-110">Przykład 1: usuwanie reguł CORS dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="3ca6c-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="3ca6c-111">To polecenie usuwa reguły CORS dla typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="3ca6c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ca6c-112">PARAMETERS</span></span>

### <span data-ttu-id="3ca6c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ca6c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3ca6c-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3ca6c-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3ca6c-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3ca6c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3ca6c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3ca6c-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3ca6c-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3ca6c-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3ca6c-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3ca6c-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="3ca6c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="3ca6c-123">-Context</span></span>
<span data-ttu-id="3ca6c-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3ca6c-125">Aby uzyskać kontekst miejsca do magazynowania, New-AzStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3ca6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca6c-126">-DefaultProfile</span></span>
<span data-ttu-id="3ca6c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca6c-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ca6c-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3ca6c-129">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3ca6c-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="3ca6c-130">-ServiceType</span></span>
<span data-ttu-id="3ca6c-131">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet usuwa reguły.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="3ca6c-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3ca6c-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ca6c-133">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="3ca6c-133">Blob</span></span> 
- <span data-ttu-id="3ca6c-134">Tworząc</span><span class="sxs-lookup"><span data-stu-id="3ca6c-134">Table</span></span> 
- <span data-ttu-id="3ca6c-135">Wykonany</span><span class="sxs-lookup"><span data-stu-id="3ca6c-135">Queue</span></span> 
- <span data-ttu-id="3ca6c-136">Plik</span><span class="sxs-lookup"><span data-stu-id="3ca6c-136">File</span></span>

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

### <span data-ttu-id="3ca6c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca6c-137">CommonParameters</span></span>
<span data-ttu-id="3ca6c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca6c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca6c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca6c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca6c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ca6c-140">INPUTS</span></span>

### <span data-ttu-id="3ca6c-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ca6c-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3ca6c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ca6c-142">OUTPUTS</span></span>

### <span data-ttu-id="3ca6c-143">System. void</span><span class="sxs-lookup"><span data-stu-id="3ca6c-143">System.Void</span></span>

## <span data-ttu-id="3ca6c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ca6c-144">NOTES</span></span>

## <span data-ttu-id="3ca6c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ca6c-145">RELATED LINKS</span></span>

[<span data-ttu-id="3ca6c-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="3ca6c-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="3ca6c-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="3ca6c-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


