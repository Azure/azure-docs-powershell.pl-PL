---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a1df300ab48a1de19b16b00c53379e05046b8588
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899399"
---
# <span data-ttu-id="8b74f-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b74f-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="8b74f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b74f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b74f-103">Aktualizuje zapisane zasady dostępu w udziale magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b74f-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b74f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b74f-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b74f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b74f-105">DESCRIPTION</span></span>
<span data-ttu-id="8b74f-106">Polecenie cmdlet **Set-AzureStorageShareStoredAccessPolicy** aktualizuje przechowywane zasady dostępu w udziale magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b74f-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="8b74f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b74f-107">EXAMPLES</span></span>

### <span data-ttu-id="8b74f-108">Przykład 1: aktualizowanie przechowywanych zasad dostępu w udziale magazynu</span><span class="sxs-lookup"><span data-stu-id="8b74f-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="8b74f-109">To polecenie aktualizuje zapisane zasady dostępu, które mają pełne uprawnienia w udziale.</span><span class="sxs-lookup"><span data-stu-id="8b74f-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="8b74f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b74f-110">PARAMETERS</span></span>

### <span data-ttu-id="8b74f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b74f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8b74f-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="8b74f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8b74f-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="8b74f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8b74f-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="8b74f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b74f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8b74f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8b74f-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8b74f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8b74f-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8b74f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8b74f-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="8b74f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8b74f-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="8b74f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8b74f-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8b74f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8b74f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="8b74f-121">-Context</span></span>
<span data-ttu-id="8b74f-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8b74f-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8b74f-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8b74f-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8b74f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b74f-124">-DefaultProfile</span></span>
<span data-ttu-id="8b74f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b74f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b74f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8b74f-126">-ExpiryTime</span></span>
<span data-ttu-id="8b74f-127">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="8b74f-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="8b74f-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8b74f-128">-NoExpiryTime</span></span>
<span data-ttu-id="8b74f-129">Wskazuje, że to polecenie cmdlet czyści Właściwość **ExpiryTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="8b74f-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="8b74f-130">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="8b74f-130">-NoStartTime</span></span>
<span data-ttu-id="8b74f-131">Wskazuje, że to polecenie cmdlet czyści Właściwość **StartTime** w przechowywanych zasadach dostępu.</span><span class="sxs-lookup"><span data-stu-id="8b74f-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="8b74f-132">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="8b74f-132">-Permission</span></span>
<span data-ttu-id="8b74f-133">Umożliwia określenie uprawnień do przechowywanych zasad dostępu w celu uzyskania dostępu do udziału lub plików znajdujących się pod nim.</span><span class="sxs-lookup"><span data-stu-id="8b74f-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="8b74f-134">Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).</span><span class="sxs-lookup"><span data-stu-id="8b74f-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8b74f-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="8b74f-135">-Policy</span></span>
<span data-ttu-id="8b74f-136">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="8b74f-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="8b74f-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b74f-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8b74f-138">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="8b74f-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8b74f-139">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="8b74f-139">-ShareName</span></span>
<span data-ttu-id="8b74f-140">Określa nazwę udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b74f-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="8b74f-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8b74f-141">-StartTime</span></span>
<span data-ttu-id="8b74f-142">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="8b74f-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8b74f-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b74f-143">-Confirm</span></span>
<span data-ttu-id="8b74f-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b74f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b74f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b74f-145">-WhatIf</span></span>
<span data-ttu-id="8b74f-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b74f-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b74f-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b74f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b74f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b74f-148">CommonParameters</span></span>
<span data-ttu-id="8b74f-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b74f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b74f-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b74f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b74f-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b74f-151">INPUTS</span></span>

### <span data-ttu-id="8b74f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8b74f-152">System.String</span></span>

### <span data-ttu-id="8b74f-153">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b74f-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8b74f-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b74f-154">OUTPUTS</span></span>

### <span data-ttu-id="8b74f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8b74f-155">System.String</span></span>

## <span data-ttu-id="8b74f-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b74f-156">NOTES</span></span>

## <span data-ttu-id="8b74f-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b74f-157">RELATED LINKS</span></span>

[<span data-ttu-id="8b74f-158">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b74f-158">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8b74f-159">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b74f-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8b74f-160">Nowe — AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b74f-160">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8b74f-161">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b74f-161">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
