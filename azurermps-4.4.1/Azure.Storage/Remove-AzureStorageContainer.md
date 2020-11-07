---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 0dce586ff0b129887924e22fdcb152d818bfc526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541428"
---
# <span data-ttu-id="1ee40-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1ee40-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="1ee40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ee40-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee40-103">Usuwa określony kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ee40-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ee40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ee40-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ee40-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee40-106">Polecenie cmdlet **Remove-AzureStorageContainer** usuwa określony kontener magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee40-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="1ee40-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ee40-107">EXAMPLES</span></span>

### <span data-ttu-id="1ee40-108">Przykład 1. Usuń kontener</span><span class="sxs-lookup"><span data-stu-id="1ee40-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="1ee40-109">W tym przykładzie usunięto kontener o nazwie MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="1ee40-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="1ee40-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ee40-110">PARAMETERS</span></span>

### <span data-ttu-id="1ee40-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1ee40-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1ee40-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="1ee40-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1ee40-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="1ee40-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1ee40-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="1ee40-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1ee40-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1ee40-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1ee40-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1ee40-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1ee40-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1ee40-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1ee40-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="1ee40-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1ee40-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="1ee40-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1ee40-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="1ee40-120">The default value is 10.</span></span>

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

### <span data-ttu-id="1ee40-121">-Context</span><span class="sxs-lookup"><span data-stu-id="1ee40-121">-Context</span></span>
<span data-ttu-id="1ee40-122">Określa kontekst kontenera, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1ee40-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="1ee40-123">Za pomocą polecenia cmdlet New-AzureStorageContext możesz je utworzyć.</span><span class="sxs-lookup"><span data-stu-id="1ee40-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="1ee40-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1ee40-124">-Force</span></span>
<span data-ttu-id="1ee40-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1ee40-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ee40-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ee40-126">-Name</span></span>
<span data-ttu-id="1ee40-127">Określa nazwę kontenera do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1ee40-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee40-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ee40-128">-PassThru</span></span>
<span data-ttu-id="1ee40-129">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="1ee40-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1ee40-130">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="1ee40-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1ee40-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1ee40-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1ee40-132">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="1ee40-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1ee40-133">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="1ee40-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1ee40-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ee40-134">-Confirm</span></span>
<span data-ttu-id="1ee40-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee40-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee40-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee40-136">-WhatIf</span></span>
<span data-ttu-id="1ee40-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee40-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ee40-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ee40-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee40-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee40-139">CommonParameters</span></span>
<span data-ttu-id="1ee40-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee40-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee40-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee40-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee40-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ee40-142">INPUTS</span></span>

### <span data-ttu-id="1ee40-143">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ee40-143">IStorageContext</span></span>

<span data-ttu-id="1ee40-144">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="1ee40-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1ee40-145">Ciąg</span><span class="sxs-lookup"><span data-stu-id="1ee40-145">String</span></span>

<span data-ttu-id="1ee40-146">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="1ee40-146">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1ee40-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ee40-147">OUTPUTS</span></span>

### <span data-ttu-id="1ee40-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ee40-148">System.Boolean</span></span>

## <span data-ttu-id="1ee40-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ee40-149">NOTES</span></span>

## <span data-ttu-id="1ee40-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ee40-150">RELATED LINKS</span></span>

[<span data-ttu-id="1ee40-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1ee40-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="1ee40-152">Nowe — AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1ee40-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)