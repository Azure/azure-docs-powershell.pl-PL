---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: b7d10ba1418ee7dd47a5dfa5256d0fecbc2e46ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704801"
---
# <span data-ttu-id="c6f45-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6f45-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="c6f45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6f45-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f45-103">Aktualizuje zapisane zasady dostępu w udziale magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6f45-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="c6f45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6f45-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6f45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6f45-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f45-106">Polecenie cmdlet **Set-AzStorageShareStoredAccessPolicy** aktualizuje przechowywane zasady dostępu w udziale magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6f45-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="c6f45-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6f45-107">EXAMPLES</span></span>

### <span data-ttu-id="c6f45-108">Przykład 1: aktualizowanie przechowywanych zasad dostępu w udziale magazynu</span><span class="sxs-lookup"><span data-stu-id="c6f45-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="c6f45-109">To polecenie aktualizuje zapisane zasady dostępu, które mają pełne uprawnienia w udziale.</span><span class="sxs-lookup"><span data-stu-id="c6f45-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="c6f45-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6f45-110">PARAMETERS</span></span>

### <span data-ttu-id="c6f45-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6f45-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c6f45-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="c6f45-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c6f45-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="c6f45-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c6f45-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="c6f45-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6f45-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c6f45-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c6f45-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c6f45-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c6f45-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c6f45-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c6f45-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="c6f45-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c6f45-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="c6f45-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c6f45-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="c6f45-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c6f45-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c6f45-121">-Context</span></span>
<span data-ttu-id="c6f45-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c6f45-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c6f45-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c6f45-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c6f45-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f45-124">-DefaultProfile</span></span>
<span data-ttu-id="c6f45-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6f45-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f45-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c6f45-126">-ExpiryTime</span></span>
<span data-ttu-id="c6f45-127">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="c6f45-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="c6f45-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c6f45-128">-NoExpiryTime</span></span>
<span data-ttu-id="c6f45-129">Wskazuje, że to polecenie cmdlet czyści Właściwość **ExpiryTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="c6f45-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="c6f45-130">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="c6f45-130">-NoStartTime</span></span>
<span data-ttu-id="c6f45-131">Wskazuje, że to polecenie cmdlet czyści Właściwość **StartTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="c6f45-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="c6f45-132">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="c6f45-132">-Permission</span></span>
<span data-ttu-id="c6f45-133">Umożliwia określenie uprawnień do przechowywanych zasad dostępu w celu uzyskania dostępu do udziału lub plików znajdujących się pod nim.</span><span class="sxs-lookup"><span data-stu-id="c6f45-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="c6f45-134">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="c6f45-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c6f45-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="c6f45-135">-Policy</span></span>
<span data-ttu-id="c6f45-136">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="c6f45-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="c6f45-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6f45-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c6f45-138">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="c6f45-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c6f45-139">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="c6f45-139">-ShareName</span></span>
<span data-ttu-id="c6f45-140">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6f45-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="c6f45-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c6f45-141">-StartTime</span></span>
<span data-ttu-id="c6f45-142">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="c6f45-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="c6f45-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6f45-143">-Confirm</span></span>
<span data-ttu-id="c6f45-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6f45-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6f45-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f45-145">-WhatIf</span></span>
<span data-ttu-id="c6f45-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6f45-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6f45-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c6f45-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6f45-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f45-148">CommonParameters</span></span>
<span data-ttu-id="c6f45-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f45-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f45-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f45-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f45-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6f45-151">INPUTS</span></span>

### <span data-ttu-id="c6f45-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f45-152">System.String</span></span>

### <span data-ttu-id="c6f45-153">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6f45-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6f45-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6f45-154">OUTPUTS</span></span>

### <span data-ttu-id="c6f45-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f45-155">System.String</span></span>

## <span data-ttu-id="c6f45-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6f45-156">NOTES</span></span>

## <span data-ttu-id="c6f45-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6f45-157">RELATED LINKS</span></span>

[<span data-ttu-id="c6f45-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6f45-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c6f45-159">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6f45-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c6f45-160">Nowe — AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6f45-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c6f45-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6f45-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
