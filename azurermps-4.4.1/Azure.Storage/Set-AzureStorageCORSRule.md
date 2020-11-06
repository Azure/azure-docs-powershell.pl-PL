---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 9b3bc0f9a0d0345662f63ef8387239e0792057e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552508"
---
# <span data-ttu-id="2c867-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="2c867-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="2c867-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c867-102">SYNOPSIS</span></span>
<span data-ttu-id="2c867-103">Ustawia reguły CORS dla typu usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c867-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c867-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c867-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2c867-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c867-105">DESCRIPTION</span></span>
<span data-ttu-id="2c867-106">Polecenie cmdlet **Set-AzureStorageCORSRule** ustawia reguły funkcji udostępniania zasobów krzyżowych (CORS) dla typu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2c867-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="2c867-107">Typy usług magazynowania dla tego polecenia cmdlet to obiekt BLOB, tabela, kolejka i plik.</span><span class="sxs-lookup"><span data-stu-id="2c867-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="2c867-108">To polecenie cmdlet zastępuje istniejące reguły.</span><span class="sxs-lookup"><span data-stu-id="2c867-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="2c867-109">Aby wyświetlić bieżące reguły, użyj polecenia cmdlet Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="2c867-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="2c867-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c867-110">EXAMPLES</span></span>

### <span data-ttu-id="2c867-111">Przykład 1: Przypisywanie reguł CORS do usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="2c867-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="2c867-112">Pierwsze polecenie umożliwia przypisanie tablicy reguł do zmiennej $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="2c867-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="2c867-113">To polecenie używa standardu rozciąganego na kilka wierszy w tym bloku kodu.</span><span class="sxs-lookup"><span data-stu-id="2c867-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="2c867-114">Drugie polecenie przypisuje reguły w $CorsRules do typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="2c867-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="2c867-115">Przykład 2: Zmienianie właściwości reguły CORS dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="2c867-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="2c867-116">Pierwsze polecenie pobiera bieżące reguły CORS dla typu obiektu BLOB przy użyciu polecenia cmdlet **Get-AzureStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="2c867-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="2c867-117">Polecenie przechowuje reguły w zmiennej tablicowej $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="2c867-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="2c867-118">Drugie i trzecie polecenia modyfikują pierwszą regułę w $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="2c867-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="2c867-119">Polecenie ostatnie umożliwia przypisanie reguł w $CorsRules do typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="2c867-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="2c867-120">Poprawione reguły zastępują bieżące reguły CORS.</span><span class="sxs-lookup"><span data-stu-id="2c867-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="2c867-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c867-121">PARAMETERS</span></span>

### <span data-ttu-id="2c867-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c867-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2c867-123">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="2c867-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2c867-124">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="2c867-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2c867-125">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="2c867-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2c867-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2c867-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2c867-127">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2c867-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2c867-128">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="2c867-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2c867-129">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="2c867-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2c867-130">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="2c867-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2c867-131">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="2c867-131">The default value is 10.</span></span>

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

### <span data-ttu-id="2c867-132">-Context</span><span class="sxs-lookup"><span data-stu-id="2c867-132">-Context</span></span>
<span data-ttu-id="2c867-133">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2c867-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="2c867-134">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2c867-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2c867-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="2c867-135">-CorsRules</span></span>
<span data-ttu-id="2c867-136">Określa tablicę reguł specyfikacji CORS.</span><span class="sxs-lookup"><span data-stu-id="2c867-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="2c867-137">Istniejące reguły można pobrać przy użyciu polecenia cmdlet Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="2c867-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c867-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c867-138">-PassThru</span></span>
<span data-ttu-id="2c867-139">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="2c867-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="2c867-140">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="2c867-140">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c867-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c867-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2c867-142">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="2c867-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2c867-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="2c867-143">-ServiceType</span></span>
<span data-ttu-id="2c867-144">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet przypisuje reguły.</span><span class="sxs-lookup"><span data-stu-id="2c867-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="2c867-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2c867-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c867-146">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="2c867-146">Blob</span></span> 
- <span data-ttu-id="2c867-147">Tworząc</span><span class="sxs-lookup"><span data-stu-id="2c867-147">Table</span></span> 
- <span data-ttu-id="2c867-148">Wykonany</span><span class="sxs-lookup"><span data-stu-id="2c867-148">Queue</span></span> 
- <span data-ttu-id="2c867-149">Plik</span><span class="sxs-lookup"><span data-stu-id="2c867-149">File</span></span>

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

### <span data-ttu-id="2c867-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c867-150">CommonParameters</span></span>
<span data-ttu-id="2c867-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c867-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c867-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c867-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c867-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c867-153">INPUTS</span></span>

### <span data-ttu-id="2c867-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c867-154">IStorageContext</span></span>

<span data-ttu-id="2c867-155">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="2c867-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="2c867-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c867-156">OUTPUTS</span></span>

### <span data-ttu-id="2c867-157">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="2c867-157">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="2c867-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c867-158">NOTES</span></span>

## <span data-ttu-id="2c867-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c867-159">RELATED LINKS</span></span>

[<span data-ttu-id="2c867-160">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="2c867-160">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="2c867-161">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c867-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2c867-162">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="2c867-162">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


