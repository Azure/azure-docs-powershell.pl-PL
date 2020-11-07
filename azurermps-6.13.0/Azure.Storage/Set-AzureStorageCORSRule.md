---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
ms.openlocfilehash: 21293b8262a10c5710ed132413658c3c1cfbd254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526429"
---
# <span data-ttu-id="c2da4-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c2da4-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="c2da4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2da4-102">SYNOPSIS</span></span>
<span data-ttu-id="c2da4-103">Ustawia reguły CORS dla typu usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2da4-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2da4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2da4-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c2da4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2da4-105">DESCRIPTION</span></span>
<span data-ttu-id="c2da4-106">Polecenie cmdlet **Set-AzureStorageCORSRule** ustawia reguły funkcji udostępniania zasobów krzyżowych (CORS) dla typu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c2da4-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="c2da4-107">Typy usług magazynowania dla tego polecenia cmdlet to obiekt BLOB, tabela, kolejka i plik.</span><span class="sxs-lookup"><span data-stu-id="c2da4-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="c2da4-108">To polecenie cmdlet zastępuje istniejące reguły.</span><span class="sxs-lookup"><span data-stu-id="c2da4-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="c2da4-109">Aby wyświetlić bieżące reguły, użyj polecenia cmdlet Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="c2da4-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="c2da4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2da4-110">EXAMPLES</span></span>

### <span data-ttu-id="c2da4-111">Przykład 1: Przypisywanie reguł CORS do usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="c2da4-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="c2da4-112">Pierwsze polecenie umożliwia przypisanie tablicy reguł do zmiennej $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="c2da4-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="c2da4-113">To polecenie używa standardu rozciąganego na kilka wierszy w tym bloku kodu.</span><span class="sxs-lookup"><span data-stu-id="c2da4-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="c2da4-114">Drugie polecenie przypisuje reguły w $CorsRules do typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="c2da4-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="c2da4-115">Przykład 2: Zmienianie właściwości reguły CORS dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="c2da4-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="c2da4-116">Pierwsze polecenie pobiera bieżące reguły CORS dla typu obiektu BLOB przy użyciu polecenia cmdlet **Get-AzureStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="c2da4-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="c2da4-117">Polecenie przechowuje reguły w zmiennej tablicowej $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="c2da4-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="c2da4-118">Drugie i trzecie polecenia modyfikują pierwszą regułę w $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="c2da4-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="c2da4-119">Polecenie ostatnie umożliwia przypisanie reguł w $CorsRules do typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="c2da4-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="c2da4-120">Poprawione reguły zastępują bieżące reguły CORS.</span><span class="sxs-lookup"><span data-stu-id="c2da4-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="c2da4-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2da4-121">PARAMETERS</span></span>

### <span data-ttu-id="c2da4-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2da4-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c2da4-123">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c2da4-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c2da4-124">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c2da4-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c2da4-125">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c2da4-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c2da4-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c2da4-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c2da4-127">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c2da4-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c2da4-128">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c2da4-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c2da4-129">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="c2da4-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c2da4-130">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c2da4-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c2da4-131">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c2da4-131">The default value is 10.</span></span>

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

### <span data-ttu-id="c2da4-132">-Context</span><span class="sxs-lookup"><span data-stu-id="c2da4-132">-Context</span></span>
<span data-ttu-id="c2da4-133">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c2da4-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c2da4-134">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c2da4-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c2da4-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="c2da4-135">-CorsRules</span></span>
<span data-ttu-id="c2da4-136">Określa tablicę reguł specyfikacji CORS.</span><span class="sxs-lookup"><span data-stu-id="c2da4-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="c2da4-137">Istniejące reguły można pobrać przy użyciu polecenia cmdlet Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="c2da4-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2da4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2da4-138">-DefaultProfile</span></span>
<span data-ttu-id="c2da4-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2da4-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2da4-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2da4-140">-PassThru</span></span>
<span data-ttu-id="c2da4-141">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="c2da4-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="c2da4-142">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="c2da4-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c2da4-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c2da4-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c2da4-144">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="c2da4-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c2da4-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c2da4-145">-ServiceType</span></span>
<span data-ttu-id="c2da4-146">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet przypisuje reguły.</span><span class="sxs-lookup"><span data-stu-id="c2da4-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="c2da4-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2da4-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2da4-148">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="c2da4-148">Blob</span></span> 
- <span data-ttu-id="c2da4-149">Tworząc</span><span class="sxs-lookup"><span data-stu-id="c2da4-149">Table</span></span> 
- <span data-ttu-id="c2da4-150">Wykonany</span><span class="sxs-lookup"><span data-stu-id="c2da4-150">Queue</span></span> 
- <span data-ttu-id="c2da4-151">Plik</span><span class="sxs-lookup"><span data-stu-id="c2da4-151">File</span></span>

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

### <span data-ttu-id="c2da4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2da4-152">CommonParameters</span></span>
<span data-ttu-id="c2da4-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2da4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2da4-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2da4-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2da4-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2da4-155">INPUTS</span></span>

### <span data-ttu-id="c2da4-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2da4-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2da4-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2da4-157">OUTPUTS</span></span>

### <span data-ttu-id="c2da4-158">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="c2da4-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="c2da4-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2da4-159">NOTES</span></span>

## <span data-ttu-id="c2da4-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2da4-160">RELATED LINKS</span></span>

[<span data-ttu-id="c2da4-161">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c2da4-161">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="c2da4-162">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2da4-162">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c2da4-163">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c2da4-163">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

