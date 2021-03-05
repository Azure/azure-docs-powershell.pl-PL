---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: 9c6213fb619297ca5e2c49883f42a5d875d940e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985538"
---
# <span data-ttu-id="5292f-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5292f-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="5292f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5292f-102">SYNOPSIS</span></span>
<span data-ttu-id="5292f-103">Usuwa cors dla usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="5292f-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="5292f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5292f-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5292f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5292f-105">DESCRIPTION</span></span>
<span data-ttu-id="5292f-106">Polecenie **cmdlet Remove-AzStorageCORSRule** usuwa usługę CORS (Cross-Origin Resource Sharing) dla usługi magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5292f-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="5292f-107">To polecenie cmdlet usuwa wszystkie reguły cors w typie usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="5292f-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="5292f-108">Typy usług magazynu dla tego polecenia cmdlet to obiekty blob, tabela, kolejkowanie i plik.</span><span class="sxs-lookup"><span data-stu-id="5292f-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="5292f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5292f-109">EXAMPLES</span></span>

### <span data-ttu-id="5292f-110">Przykład 1. Usuwanie reguł CORS dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="5292f-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="5292f-111">To polecenie usuwa reguły CORS dla typu usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="5292f-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="5292f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5292f-112">PARAMETERS</span></span>

### <span data-ttu-id="5292f-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5292f-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5292f-114">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="5292f-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5292f-115">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="5292f-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5292f-116">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="5292f-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5292f-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5292f-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5292f-118">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5292f-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5292f-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5292f-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5292f-120">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="5292f-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5292f-121">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="5292f-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5292f-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="5292f-122">The default value is 10.</span></span>

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

### <span data-ttu-id="5292f-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5292f-123">-Context</span></span>
<span data-ttu-id="5292f-124">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5292f-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5292f-125">Aby uzyskać kontekst magazynu, należy New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5292f-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5292f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5292f-126">-DefaultProfile</span></span>
<span data-ttu-id="5292f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5292f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5292f-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5292f-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5292f-129">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="5292f-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5292f-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5292f-130">-ServiceType</span></span>
<span data-ttu-id="5292f-131">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet usuwa reguły.</span><span class="sxs-lookup"><span data-stu-id="5292f-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="5292f-132">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5292f-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5292f-133">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="5292f-133">Blob</span></span> 
- <span data-ttu-id="5292f-134">Tabela</span><span class="sxs-lookup"><span data-stu-id="5292f-134">Table</span></span> 
- <span data-ttu-id="5292f-135">Kolejka</span><span class="sxs-lookup"><span data-stu-id="5292f-135">Queue</span></span> 
- <span data-ttu-id="5292f-136">Plik</span><span class="sxs-lookup"><span data-stu-id="5292f-136">File</span></span>

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

### <span data-ttu-id="5292f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5292f-137">CommonParameters</span></span>
<span data-ttu-id="5292f-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5292f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5292f-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5292f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5292f-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5292f-140">INPUTS</span></span>

### <span data-ttu-id="5292f-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5292f-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5292f-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5292f-142">OUTPUTS</span></span>

### <span data-ttu-id="5292f-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="5292f-143">System.Void</span></span>

## <span data-ttu-id="5292f-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5292f-144">NOTES</span></span>

## <span data-ttu-id="5292f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5292f-145">RELATED LINKS</span></span>

[<span data-ttu-id="5292f-146">Get-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5292f-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="5292f-147">Set-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5292f-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


