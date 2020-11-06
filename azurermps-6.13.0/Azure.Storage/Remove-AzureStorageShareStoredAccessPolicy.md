---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 64eb11604d1b75682b95851f87ff8aa9d2b26466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547764"
---
# <span data-ttu-id="37754-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="37754-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="37754-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37754-102">SYNOPSIS</span></span>
<span data-ttu-id="37754-103">Usuwa zapisane zasady dostępu z udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="37754-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37754-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37754-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37754-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37754-105">DESCRIPTION</span></span>
<span data-ttu-id="37754-106">Polecenie cmdlet **Remove-AzureStorageShareStoredAccessPolicy** usuwa zapisane zasady dostępu z udziału w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="37754-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="37754-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37754-107">EXAMPLES</span></span>

### <span data-ttu-id="37754-108">Przykład 1: usuwanie zapisanych zasad dostępu z udziału w usłudze Azure Storage</span><span class="sxs-lookup"><span data-stu-id="37754-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="37754-109">To polecenie usuwa zapisane zasady dostępu o nazwie GeneralPolicy z ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="37754-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="37754-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37754-110">PARAMETERS</span></span>

### <span data-ttu-id="37754-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37754-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="37754-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="37754-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="37754-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="37754-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="37754-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="37754-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="37754-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="37754-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="37754-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="37754-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="37754-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="37754-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="37754-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="37754-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="37754-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="37754-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="37754-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="37754-120">The default value is 10.</span></span>

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

### <span data-ttu-id="37754-121">-Context</span><span class="sxs-lookup"><span data-stu-id="37754-121">-Context</span></span>
<span data-ttu-id="37754-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="37754-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="37754-123">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="37754-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="37754-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37754-124">-DefaultProfile</span></span>
<span data-ttu-id="37754-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37754-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37754-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37754-126">-PassThru</span></span>
<span data-ttu-id="37754-127">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="37754-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="37754-128">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="37754-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="37754-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="37754-129">-Policy</span></span>
<span data-ttu-id="37754-130">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37754-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37754-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37754-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="37754-132">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="37754-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="37754-133">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="37754-133">-ShareName</span></span>
<span data-ttu-id="37754-134">Określa nazwę udziału w magazynie, dla którego to polecenie cmdlet usuwa zasady.</span><span class="sxs-lookup"><span data-stu-id="37754-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37754-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37754-135">-Confirm</span></span>
<span data-ttu-id="37754-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37754-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37754-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37754-137">-WhatIf</span></span>
<span data-ttu-id="37754-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37754-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37754-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37754-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37754-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37754-140">CommonParameters</span></span>
<span data-ttu-id="37754-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37754-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37754-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37754-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37754-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37754-143">INPUTS</span></span>

### <span data-ttu-id="37754-144">System. String</span><span class="sxs-lookup"><span data-stu-id="37754-144">System.String</span></span>

### <span data-ttu-id="37754-145">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="37754-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="37754-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37754-146">OUTPUTS</span></span>

### <span data-ttu-id="37754-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37754-147">System.Boolean</span></span>

## <span data-ttu-id="37754-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37754-148">NOTES</span></span>

## <span data-ttu-id="37754-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37754-149">RELATED LINKS</span></span>

[<span data-ttu-id="37754-150">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="37754-150">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="37754-151">Nowe — AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="37754-151">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="37754-152">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="37754-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="37754-153">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="37754-153">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
