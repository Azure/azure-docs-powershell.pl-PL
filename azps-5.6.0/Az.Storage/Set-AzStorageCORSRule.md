---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: 6a04b038a452d979394ab57d8f3d905a57428051
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976145"
---
# <span data-ttu-id="a0173-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a0173-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="a0173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0173-102">SYNOPSIS</span></span>
<span data-ttu-id="a0173-103">Ustawia reguły CORS dla typu usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0173-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="a0173-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0173-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a0173-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0173-105">DESCRIPTION</span></span>
<span data-ttu-id="a0173-106">Polecenie **cmdlet Set-AzStorageCORSRule** ustawia reguły CORS (Cross-Origin Resource Sharing) dla typu usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a0173-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="a0173-107">Typy usług magazynu dla tego polecenia cmdlet to obiekty blob, tabela, kolejkowanie i plik.</span><span class="sxs-lookup"><span data-stu-id="a0173-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="a0173-108">To polecenie cmdlet zastępuje istniejące reguły.</span><span class="sxs-lookup"><span data-stu-id="a0173-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="a0173-109">Aby wyświetlić bieżące reguły, użyj Get-AzStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0173-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="a0173-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0173-110">EXAMPLES</span></span>

### <span data-ttu-id="a0173-111">Przykład 1. Przypisywanie reguł CORS do usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="a0173-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="a0173-112">Pierwsze polecenie przypisuje tablicę reguł do zmiennej $CorsRules zmienną.</span><span class="sxs-lookup"><span data-stu-id="a0173-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="a0173-113">To polecenie używa standardowego rozsuwu na kilku wierszach tego bloku kodu.</span><span class="sxs-lookup"><span data-stu-id="a0173-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="a0173-114">Drugie polecenie przypisuje reguły w $CorsRules do typu usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="a0173-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="a0173-115">Przykład 2. Zmienianie właściwości reguły CORS dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="a0173-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="a0173-116">Pierwsze polecenie pobiera bieżące reguły CORS dla typu obiektu blob przy użyciu polecenia cmdlet **Get-AzStorageCORSRule.**</span><span class="sxs-lookup"><span data-stu-id="a0173-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="a0173-117">Polecenie przechowuje reguły w $CorsRules tablicowej.</span><span class="sxs-lookup"><span data-stu-id="a0173-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="a0173-118">Drugie i trzecie polecenia modyfikują pierwszą regułę w $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="a0173-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="a0173-119">Ostatnie polecenie przypisuje reguły z $CorsRules do typu usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="a0173-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="a0173-120">Zmienione reguły zastępują bieżące reguły cors.</span><span class="sxs-lookup"><span data-stu-id="a0173-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="a0173-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0173-121">PARAMETERS</span></span>

### <span data-ttu-id="a0173-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0173-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0173-123">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="a0173-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0173-124">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="a0173-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0173-125">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="a0173-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0173-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0173-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0173-127">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a0173-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0173-128">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="a0173-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0173-129">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="a0173-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0173-130">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="a0173-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0173-131">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="a0173-131">The default value is 10.</span></span>

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

### <span data-ttu-id="a0173-132">— kontekst</span><span class="sxs-lookup"><span data-stu-id="a0173-132">-Context</span></span>
<span data-ttu-id="a0173-133">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a0173-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a0173-134">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0173-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a0173-135">- CorsRules</span><span class="sxs-lookup"><span data-stu-id="a0173-135">-CorsRules</span></span>
<span data-ttu-id="a0173-136">Określa tablicę reguł CORS.</span><span class="sxs-lookup"><span data-stu-id="a0173-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="a0173-137">Istniejące reguły można pobrać za pomocą Get-AzStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0173-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="a0173-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0173-138">-DefaultProfile</span></span>
<span data-ttu-id="a0173-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0173-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0173-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0173-140">-PassThru</span></span>
<span data-ttu-id="a0173-141">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="a0173-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="a0173-142">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="a0173-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a0173-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0173-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0173-144">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="a0173-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a0173-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a0173-145">-ServiceType</span></span>
<span data-ttu-id="a0173-146">Określa typ usługi Azure Storage, do której to polecenie cmdlet przypisuje reguły.</span><span class="sxs-lookup"><span data-stu-id="a0173-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="a0173-147">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a0173-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0173-148">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="a0173-148">Blob</span></span> 
- <span data-ttu-id="a0173-149">Tabela</span><span class="sxs-lookup"><span data-stu-id="a0173-149">Table</span></span> 
- <span data-ttu-id="a0173-150">Kolejka</span><span class="sxs-lookup"><span data-stu-id="a0173-150">Queue</span></span> 
- <span data-ttu-id="a0173-151">Plik</span><span class="sxs-lookup"><span data-stu-id="a0173-151">File</span></span>

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

### <span data-ttu-id="a0173-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0173-152">CommonParameters</span></span>
<span data-ttu-id="a0173-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0173-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0173-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0173-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0173-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0173-155">INPUTS</span></span>

### <span data-ttu-id="a0173-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0173-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0173-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0173-157">OUTPUTS</span></span>

### <span data-ttu-id="a0173-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="a0173-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="a0173-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0173-159">NOTES</span></span>

## <span data-ttu-id="a0173-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0173-160">RELATED LINKS</span></span>

[<span data-ttu-id="a0173-161">Get-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a0173-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="a0173-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0173-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a0173-163">Remove-azstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a0173-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


