---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: 3b2347ae13312f079cee1328fe504644e3cf4e15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704813"
---
# <span data-ttu-id="68b99-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="68b99-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="68b99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68b99-102">SYNOPSIS</span></span>
<span data-ttu-id="68b99-103">Ustawia reguły CORS dla typu usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="68b99-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="68b99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68b99-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="68b99-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68b99-105">DESCRIPTION</span></span>
<span data-ttu-id="68b99-106">Polecenie cmdlet **Set-AzStorageCORSRule** ustawia reguły funkcji udostępniania zasobów krzyżowych (CORS) dla typu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="68b99-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="68b99-107">Typy usług magazynowania dla tego polecenia cmdlet to obiekt BLOB, tabela, kolejka i plik.</span><span class="sxs-lookup"><span data-stu-id="68b99-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="68b99-108">To polecenie cmdlet zastępuje istniejące reguły.</span><span class="sxs-lookup"><span data-stu-id="68b99-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="68b99-109">Aby wyświetlić bieżące reguły, użyj polecenia cmdlet Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="68b99-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="68b99-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68b99-110">EXAMPLES</span></span>

### <span data-ttu-id="68b99-111">Przykład 1: Przypisywanie reguł CORS do usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="68b99-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="68b99-112">Pierwsze polecenie umożliwia przypisanie tablicy reguł do zmiennej $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="68b99-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="68b99-113">To polecenie używa standardu rozciąganego na kilka wierszy w tym bloku kodu.</span><span class="sxs-lookup"><span data-stu-id="68b99-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="68b99-114">Drugie polecenie przypisuje reguły w $CorsRules do typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="68b99-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="68b99-115">Przykład 2: Zmienianie właściwości reguły CORS dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="68b99-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="68b99-116">Pierwsze polecenie pobiera bieżące reguły CORS dla typu obiektu BLOB przy użyciu polecenia cmdlet **Get-AzStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="68b99-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="68b99-117">Polecenie przechowuje reguły w zmiennej tablicowej $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="68b99-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="68b99-118">Drugie i trzecie polecenia modyfikują pierwszą regułę w $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="68b99-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="68b99-119">Polecenie ostatnie umożliwia przypisanie reguł w $CorsRules do typu usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="68b99-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="68b99-120">Poprawione reguły zastępują bieżące reguły CORS.</span><span class="sxs-lookup"><span data-stu-id="68b99-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="68b99-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68b99-121">PARAMETERS</span></span>

### <span data-ttu-id="68b99-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68b99-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="68b99-123">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="68b99-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="68b99-124">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="68b99-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="68b99-125">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="68b99-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="68b99-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="68b99-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="68b99-127">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="68b99-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="68b99-128">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="68b99-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="68b99-129">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="68b99-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="68b99-130">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="68b99-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="68b99-131">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="68b99-131">The default value is 10.</span></span>

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

### <span data-ttu-id="68b99-132">-Context</span><span class="sxs-lookup"><span data-stu-id="68b99-132">-Context</span></span>
<span data-ttu-id="68b99-133">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="68b99-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="68b99-134">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="68b99-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="68b99-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="68b99-135">-CorsRules</span></span>
<span data-ttu-id="68b99-136">Określa tablicę reguł specyfikacji CORS.</span><span class="sxs-lookup"><span data-stu-id="68b99-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="68b99-137">Istniejące reguły można pobrać przy użyciu polecenia cmdlet Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="68b99-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="68b99-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b99-138">-DefaultProfile</span></span>
<span data-ttu-id="68b99-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68b99-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b99-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68b99-140">-PassThru</span></span>
<span data-ttu-id="68b99-141">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="68b99-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="68b99-142">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="68b99-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="68b99-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68b99-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="68b99-144">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="68b99-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="68b99-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="68b99-145">-ServiceType</span></span>
<span data-ttu-id="68b99-146">Określa typ usługi Azure Storage, dla którego to polecenie cmdlet przypisuje reguły.</span><span class="sxs-lookup"><span data-stu-id="68b99-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="68b99-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="68b99-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68b99-148">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="68b99-148">Blob</span></span> 
- <span data-ttu-id="68b99-149">Tworząc</span><span class="sxs-lookup"><span data-stu-id="68b99-149">Table</span></span> 
- <span data-ttu-id="68b99-150">Wykonany</span><span class="sxs-lookup"><span data-stu-id="68b99-150">Queue</span></span> 
- <span data-ttu-id="68b99-151">Plik</span><span class="sxs-lookup"><span data-stu-id="68b99-151">File</span></span>

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

### <span data-ttu-id="68b99-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b99-152">CommonParameters</span></span>
<span data-ttu-id="68b99-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b99-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b99-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b99-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b99-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68b99-155">INPUTS</span></span>

### <span data-ttu-id="68b99-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="68b99-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="68b99-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68b99-157">OUTPUTS</span></span>

### <span data-ttu-id="68b99-158">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="68b99-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="68b99-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68b99-159">NOTES</span></span>

## <span data-ttu-id="68b99-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68b99-160">RELATED LINKS</span></span>

[<span data-ttu-id="68b99-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="68b99-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="68b99-162">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="68b99-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="68b99-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="68b99-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

