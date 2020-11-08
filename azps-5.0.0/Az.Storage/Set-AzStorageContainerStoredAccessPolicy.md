---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224733"
---
# <span data-ttu-id="59eee-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59eee-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="59eee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59eee-102">SYNOPSIS</span></span>
<span data-ttu-id="59eee-103">Ustawia zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="59eee-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="59eee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59eee-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59eee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="59eee-105">DESCRIPTION</span></span>
<span data-ttu-id="59eee-106">Polecenie cmdlet **Set-AzStorageContainerStoredAccessPolicy** ustawia zapisane zasady dostępu dla kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="59eee-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="59eee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59eee-107">EXAMPLES</span></span>

### <span data-ttu-id="59eee-108">Przykład 1: Ustawianie zasad dostępu przechowywanych w kontenerze magazynu z pełnymi uprawnieniami</span><span class="sxs-lookup"><span data-stu-id="59eee-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="59eee-109">To polecenie ustawia zasady dostępu o nazwie Policy06 dla kontenera magazynu o nazwie.</span><span class="sxs-lookup"><span data-stu-id="59eee-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="59eee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59eee-110">PARAMETERS</span></span>

### <span data-ttu-id="59eee-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59eee-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="59eee-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="59eee-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="59eee-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="59eee-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="59eee-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="59eee-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="59eee-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="59eee-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="59eee-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="59eee-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="59eee-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="59eee-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="59eee-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="59eee-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="59eee-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="59eee-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="59eee-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="59eee-120">The default value is 10.</span></span>

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

### <span data-ttu-id="59eee-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="59eee-121">-Container</span></span>
<span data-ttu-id="59eee-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="59eee-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59eee-123">-Context</span><span class="sxs-lookup"><span data-stu-id="59eee-123">-Context</span></span>
<span data-ttu-id="59eee-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="59eee-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="59eee-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="59eee-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="59eee-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59eee-126">-DefaultProfile</span></span>
<span data-ttu-id="59eee-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59eee-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59eee-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="59eee-128">-ExpiryTime</span></span>
<span data-ttu-id="59eee-129">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="59eee-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eee-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="59eee-130">-NoExpiryTime</span></span>
<span data-ttu-id="59eee-131">Wskazuje, że zasady dostępu nie mają daty wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="59eee-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="59eee-132">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="59eee-132">-NoStartTime</span></span>
<span data-ttu-id="59eee-133">Umożliwia ustawienie godziny rozpoczęcia $Null.</span><span class="sxs-lookup"><span data-stu-id="59eee-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="59eee-134">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="59eee-134">-Permission</span></span>
<span data-ttu-id="59eee-135">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskania dostępu do kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="59eee-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="59eee-136">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="59eee-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eee-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="59eee-137">-Policy</span></span>
<span data-ttu-id="59eee-138">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="59eee-138">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eee-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59eee-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="59eee-140">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="59eee-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="59eee-141">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="59eee-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="59eee-142">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="59eee-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="59eee-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="59eee-143">-StartTime</span></span>
<span data-ttu-id="59eee-144">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="59eee-144">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eee-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59eee-145">-Confirm</span></span>
<span data-ttu-id="59eee-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59eee-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eee-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59eee-147">-WhatIf</span></span>
<span data-ttu-id="59eee-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59eee-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59eee-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59eee-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eee-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59eee-150">CommonParameters</span></span>
<span data-ttu-id="59eee-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59eee-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59eee-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59eee-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59eee-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59eee-153">INPUTS</span></span>

### <span data-ttu-id="59eee-154">System. String</span><span class="sxs-lookup"><span data-stu-id="59eee-154">System.String</span></span>

### <span data-ttu-id="59eee-155">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59eee-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59eee-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59eee-156">OUTPUTS</span></span>

### <span data-ttu-id="59eee-157">System. String</span><span class="sxs-lookup"><span data-stu-id="59eee-157">System.String</span></span>

## <span data-ttu-id="59eee-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59eee-158">NOTES</span></span>

## <span data-ttu-id="59eee-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59eee-159">RELATED LINKS</span></span>

[<span data-ttu-id="59eee-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59eee-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="59eee-161">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59eee-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="59eee-162">Nowe — AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59eee-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="59eee-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="59eee-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
