---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: e4313dda57632fbc2a5381b1f92067da85c1a905
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002650"
---
# <span data-ttu-id="b2d6f-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="b2d6f-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="b2d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d6f-103">Pobiera reguły CORS dla typu usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="b2d6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2d6f-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b2d6f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d6f-106">Polecenie **cmdlet Get-AzStorageCORSRule** pobiera reguły CORS (Cross-Origin Resource Sharing) dla typu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="b2d6f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d6f-108">Przykład 1. Uzyskiwanie reguł CORS usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="b2d6f-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="b2d6f-109">To polecenie pobiera reguły CORS dla typu usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="b2d6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2d6f-110">PARAMETERS</span></span>

### <span data-ttu-id="b2d6f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b2d6f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b2d6f-112">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b2d6f-113">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b2d6f-114">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b2d6f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b2d6f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b2d6f-116">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b2d6f-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b2d6f-118">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b2d6f-119">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b2d6f-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b2d6f-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b2d6f-121">-Context</span></span>
<span data-ttu-id="b2d6f-122">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b2d6f-123">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b2d6f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d6f-124">-DefaultProfile</span></span>
<span data-ttu-id="b2d6f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2d6f-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b2d6f-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b2d6f-127">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b2d6f-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b2d6f-128">-ServiceType</span></span>
<span data-ttu-id="b2d6f-129">Określa typ usługi Magazynu Azure, dla którego to polecenie cmdlet pobiera reguły CORS.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="b2d6f-130">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b2d6f-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2d6f-131">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="b2d6f-131">Blob</span></span> 
- <span data-ttu-id="b2d6f-132">Tabela</span><span class="sxs-lookup"><span data-stu-id="b2d6f-132">Table</span></span> 
- <span data-ttu-id="b2d6f-133">Kolejka</span><span class="sxs-lookup"><span data-stu-id="b2d6f-133">Queue</span></span> 
- <span data-ttu-id="b2d6f-134">Plik</span><span class="sxs-lookup"><span data-stu-id="b2d6f-134">File</span></span>

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

### <span data-ttu-id="b2d6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d6f-135">CommonParameters</span></span>
<span data-ttu-id="b2d6f-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d6f-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d6f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d6f-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2d6f-138">INPUTS</span></span>

### <span data-ttu-id="b2d6f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b2d6f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b2d6f-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2d6f-140">OUTPUTS</span></span>

### <span data-ttu-id="b2d6f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="b2d6f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="b2d6f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2d6f-142">NOTES</span></span>

## <span data-ttu-id="b2d6f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2d6f-143">RELATED LINKS</span></span>

[<span data-ttu-id="b2d6f-144">Remove-azstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="b2d6f-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="b2d6f-145">Set-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="b2d6f-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


