---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 08b3ec17476e959aa7190cfb914468eb8ab73775
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717133"
---
# <span data-ttu-id="6e172-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e172-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="6e172-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e172-102">SYNOPSIS</span></span>
<span data-ttu-id="6e172-103">Usuwa zapisane zasady dostępu z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e172-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e172-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e172-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e172-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e172-105">DESCRIPTION</span></span>
<span data-ttu-id="6e172-106">Polecenie cmdlet **Remove-AzureStorageContainerStoredAccessPolicy** usuwa zapisane zasady dostępu z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e172-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="6e172-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e172-107">EXAMPLES</span></span>

### <span data-ttu-id="6e172-108">Przykład 1: usuwanie zapisanych zasad dostępu z kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="6e172-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="6e172-109">To polecenie usuwa zasady dostępu o nazwie Policy03 z kontenera przechowywanego o nazwie.</span><span class="sxs-lookup"><span data-stu-id="6e172-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="6e172-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e172-110">PARAMETERS</span></span>

### <span data-ttu-id="6e172-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e172-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6e172-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="6e172-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6e172-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="6e172-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6e172-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="6e172-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6e172-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6e172-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6e172-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6e172-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6e172-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6e172-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6e172-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="6e172-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6e172-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="6e172-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6e172-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="6e172-120">The default value is 10.</span></span>

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

### <span data-ttu-id="6e172-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="6e172-121">-Container</span></span>
<span data-ttu-id="6e172-122">Określa nazwę kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e172-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e172-123">-Context</span><span class="sxs-lookup"><span data-stu-id="6e172-123">-Context</span></span>
<span data-ttu-id="6e172-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6e172-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6e172-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6e172-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e172-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e172-126">-PassThru</span></span>
<span data-ttu-id="6e172-127">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="6e172-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6e172-128">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="6e172-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6e172-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="6e172-129">-Policy</span></span>
<span data-ttu-id="6e172-130">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e172-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e172-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e172-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6e172-132">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="6e172-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6e172-133">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="6e172-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6e172-134">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="6e172-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6e172-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e172-135">-Confirm</span></span>
<span data-ttu-id="6e172-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e172-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e172-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e172-137">-WhatIf</span></span>
<span data-ttu-id="6e172-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e172-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e172-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e172-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e172-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e172-140">CommonParameters</span></span>
<span data-ttu-id="6e172-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e172-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e172-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e172-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e172-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e172-143">INPUTS</span></span>

### <span data-ttu-id="6e172-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e172-144">IStorageContext</span></span>

<span data-ttu-id="6e172-145">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="6e172-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="6e172-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e172-146">OUTPUTS</span></span>

### <span data-ttu-id="6e172-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e172-147">System.Boolean</span></span>

## <span data-ttu-id="6e172-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e172-148">NOTES</span></span>

## <span data-ttu-id="6e172-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e172-149">RELATED LINKS</span></span>

[<span data-ttu-id="6e172-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e172-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="6e172-151">Nowe — AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e172-151">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="6e172-152">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e172-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="6e172-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e172-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)