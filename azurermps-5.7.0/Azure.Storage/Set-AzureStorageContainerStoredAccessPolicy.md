---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: d0ca5bcc01d8cf34ce22e0e91e99f0144900231c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549039"
---
# <span data-ttu-id="cc4ea-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc4ea-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="cc4ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4ea-103">Ustawia zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc4ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc4ea-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc4ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc4ea-105">DESCRIPTION</span></span>
<span data-ttu-id="cc4ea-106">Polecenie cmdlet **Set-AzureStorageContainerStoredAccessPolicy** ustawia zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="cc4ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc4ea-107">EXAMPLES</span></span>

### <span data-ttu-id="cc4ea-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w kontenerze magazynu z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="cc4ea-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="cc4ea-109">To polecenie ustawia zasady dostępu o nazwie Policy06 dla kontenera magazynu o nazwie.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="cc4ea-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc4ea-110">PARAMETERS</span></span>

### <span data-ttu-id="cc4ea-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cc4ea-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cc4ea-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cc4ea-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cc4ea-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cc4ea-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cc4ea-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cc4ea-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cc4ea-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cc4ea-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cc4ea-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cc4ea-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-120">The default value is 10.</span></span>

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

### <span data-ttu-id="cc4ea-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="cc4ea-121">-Container</span></span>
<span data-ttu-id="cc4ea-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc4ea-123">-Context</span><span class="sxs-lookup"><span data-stu-id="cc4ea-123">-Context</span></span>
<span data-ttu-id="cc4ea-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cc4ea-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cc4ea-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cc4ea-126">-ExpiryTime</span></span>
<span data-ttu-id="cc4ea-127">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4ea-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cc4ea-128">-NoExpiryTime</span></span>
<span data-ttu-id="cc4ea-129">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="cc4ea-130">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="cc4ea-130">-NoStartTime</span></span>
<span data-ttu-id="cc4ea-131">Umożliwia ustawienie godziny rozpoczęcia $Null.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="cc4ea-132">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="cc4ea-132">-Permission</span></span>
<span data-ttu-id="cc4ea-133">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskania dostępu do kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4ea-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="cc4ea-134">-Policy</span></span>
<span data-ttu-id="cc4ea-135">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-135">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4ea-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cc4ea-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cc4ea-137">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cc4ea-138">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cc4ea-139">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cc4ea-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cc4ea-140">-StartTime</span></span>
<span data-ttu-id="cc4ea-141">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-141">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4ea-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc4ea-142">-Confirm</span></span>
<span data-ttu-id="cc4ea-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4ea-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc4ea-144">-WhatIf</span></span>
<span data-ttu-id="cc4ea-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc4ea-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc4ea-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4ea-147">CommonParameters</span></span>
<span data-ttu-id="cc4ea-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc4ea-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4ea-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc4ea-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4ea-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc4ea-150">INPUTS</span></span>

### <span data-ttu-id="cc4ea-151">Ciąg</span><span class="sxs-lookup"><span data-stu-id="cc4ea-151">String</span></span>

<span data-ttu-id="cc4ea-152">Parametr "Container" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="cc4ea-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="cc4ea-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc4ea-153">IStorageContext</span></span>

<span data-ttu-id="cc4ea-154">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="cc4ea-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="cc4ea-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc4ea-155">OUTPUTS</span></span>

### <span data-ttu-id="cc4ea-156">System. String</span><span class="sxs-lookup"><span data-stu-id="cc4ea-156">System.String</span></span>

## <span data-ttu-id="cc4ea-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc4ea-157">NOTES</span></span>

## <span data-ttu-id="cc4ea-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc4ea-158">RELATED LINKS</span></span>

[<span data-ttu-id="cc4ea-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc4ea-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="cc4ea-160">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cc4ea-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="cc4ea-161">Nowe — AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc4ea-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="cc4ea-162">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cc4ea-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)