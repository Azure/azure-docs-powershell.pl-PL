---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 0c77d2dedadd205a659bf296e02c09b98342dcc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719480"
---
# <span data-ttu-id="58ea2-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="58ea2-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="58ea2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="58ea2-103">Aktualizuje zapisane zasady dostępu w udziale magazynu.</span><span class="sxs-lookup"><span data-stu-id="58ea2-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58ea2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58ea2-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ea2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58ea2-105">DESCRIPTION</span></span>
<span data-ttu-id="58ea2-106">Polecenie cmdlet **Set-AzureStorageShareStoredAccessPolicy** aktualizuje przechowywane zasady dostępu w udziale magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="58ea2-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="58ea2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58ea2-107">EXAMPLES</span></span>

### <span data-ttu-id="58ea2-108">Przykład 1: aktualizowanie przechowywanych zasad dostępu w udziale magazynu</span><span class="sxs-lookup"><span data-stu-id="58ea2-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="58ea2-109">To polecenie aktualizuje zapisane zasady dostępu, które mają pełne uprawnienia w udziale.</span><span class="sxs-lookup"><span data-stu-id="58ea2-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="58ea2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58ea2-110">PARAMETERS</span></span>

### <span data-ttu-id="58ea2-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58ea2-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="58ea2-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="58ea2-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="58ea2-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="58ea2-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="58ea2-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="58ea2-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="58ea2-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="58ea2-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="58ea2-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="58ea2-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="58ea2-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="58ea2-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="58ea2-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="58ea2-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="58ea2-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="58ea2-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="58ea2-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="58ea2-120">The default value is 10.</span></span>

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

### <span data-ttu-id="58ea2-121">-Context</span><span class="sxs-lookup"><span data-stu-id="58ea2-121">-Context</span></span>
<span data-ttu-id="58ea2-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="58ea2-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="58ea2-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="58ea2-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="58ea2-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="58ea2-124">-ExpiryTime</span></span>
<span data-ttu-id="58ea2-125">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="58ea2-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="58ea2-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="58ea2-126">-NoExpiryTime</span></span>
<span data-ttu-id="58ea2-127">Wskazuje, że to polecenie cmdlet czyści Właściwość **ExpiryTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="58ea2-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="58ea2-128">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="58ea2-128">-NoStartTime</span></span>
<span data-ttu-id="58ea2-129">Wskazuje, że to polecenie cmdlet czyści Właściwość **StartTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="58ea2-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="58ea2-130">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="58ea2-130">-Permission</span></span>
<span data-ttu-id="58ea2-131">Umożliwia określenie uprawnień do przechowywanych zasad dostępu w celu uzyskania dostępu do udziału lub plików znajdujących się pod nim.</span><span class="sxs-lookup"><span data-stu-id="58ea2-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="58ea2-132">-Policy</span><span class="sxs-lookup"><span data-stu-id="58ea2-132">-Policy</span></span>
<span data-ttu-id="58ea2-133">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="58ea2-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="58ea2-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58ea2-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="58ea2-135">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="58ea2-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="58ea2-136">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="58ea2-136">-ShareName</span></span>
<span data-ttu-id="58ea2-137">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="58ea2-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="58ea2-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="58ea2-138">-StartTime</span></span>
<span data-ttu-id="58ea2-139">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="58ea2-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="58ea2-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58ea2-140">-Confirm</span></span>
<span data-ttu-id="58ea2-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58ea2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ea2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ea2-142">-WhatIf</span></span>
<span data-ttu-id="58ea2-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58ea2-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58ea2-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58ea2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ea2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ea2-145">CommonParameters</span></span>
<span data-ttu-id="58ea2-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ea2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ea2-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ea2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ea2-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58ea2-148">INPUTS</span></span>

### <span data-ttu-id="58ea2-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="58ea2-149">IStorageContext</span></span>

<span data-ttu-id="58ea2-150">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="58ea2-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="58ea2-151">Ciąg</span><span class="sxs-lookup"><span data-stu-id="58ea2-151">String</span></span>

<span data-ttu-id="58ea2-152">Parametr "nazwa_udziału" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="58ea2-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="58ea2-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58ea2-153">OUTPUTS</span></span>

### <span data-ttu-id="58ea2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="58ea2-154">System.String</span></span>

## <span data-ttu-id="58ea2-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58ea2-155">NOTES</span></span>

## <span data-ttu-id="58ea2-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58ea2-156">RELATED LINKS</span></span>

[<span data-ttu-id="58ea2-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="58ea2-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="58ea2-158">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="58ea2-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="58ea2-159">Nowe — AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="58ea2-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="58ea2-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="58ea2-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
