---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ccaa0ef1ce2a29851d6e90235e4564df3bde876
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523017"
---
# <span data-ttu-id="78c71-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="78c71-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="78c71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78c71-102">SYNOPSIS</span></span>
<span data-ttu-id="78c71-103">Usuwa określony kontener magazynu.</span><span class="sxs-lookup"><span data-stu-id="78c71-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="78c71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78c71-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c71-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78c71-105">DESCRIPTION</span></span>
<span data-ttu-id="78c71-106">Polecenie cmdlet **Remove-AzureStorageContainer** usuwa określony kontener magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="78c71-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="78c71-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78c71-107">EXAMPLES</span></span>

### <span data-ttu-id="78c71-108">Przykład 1. Usuń kontener</span><span class="sxs-lookup"><span data-stu-id="78c71-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="78c71-109">W tym przykładzie usunięto kontener o nazwie MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="78c71-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="78c71-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78c71-110">PARAMETERS</span></span>

### <span data-ttu-id="78c71-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78c71-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="78c71-112">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="78c71-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="78c71-113">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="78c71-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="78c71-114">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="78c71-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="78c71-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="78c71-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="78c71-116">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="78c71-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="78c71-117">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="78c71-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="78c71-118">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="78c71-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="78c71-119">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="78c71-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="78c71-120">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="78c71-120">The default value is 10.</span></span>

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

### <span data-ttu-id="78c71-121">-Context</span><span class="sxs-lookup"><span data-stu-id="78c71-121">-Context</span></span>
<span data-ttu-id="78c71-122">Określa kontekst kontenera, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="78c71-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="78c71-123">Za pomocą polecenia cmdlet New-AzureStorageContext możesz je utworzyć.</span><span class="sxs-lookup"><span data-stu-id="78c71-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="78c71-124">-Force</span><span class="sxs-lookup"><span data-stu-id="78c71-124">-Force</span></span>
<span data-ttu-id="78c71-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="78c71-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="78c71-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78c71-126">-Name</span></span>
<span data-ttu-id="78c71-127">Określa nazwę kontenera do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="78c71-127">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="78c71-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78c71-128">-PassThru</span></span>
<span data-ttu-id="78c71-129">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="78c71-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="78c71-130">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="78c71-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="78c71-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78c71-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="78c71-132">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="78c71-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="78c71-133">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="78c71-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="78c71-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78c71-134">-Confirm</span></span>
<span data-ttu-id="78c71-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78c71-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c71-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c71-136">-WhatIf</span></span>
<span data-ttu-id="78c71-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78c71-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c71-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78c71-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c71-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c71-139">CommonParameters</span></span>
<span data-ttu-id="78c71-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c71-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c71-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c71-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c71-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78c71-142">INPUTS</span></span>

## <span data-ttu-id="78c71-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78c71-143">OUTPUTS</span></span>

## <span data-ttu-id="78c71-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78c71-144">NOTES</span></span>

## <span data-ttu-id="78c71-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78c71-145">RELATED LINKS</span></span>

[<span data-ttu-id="78c71-146">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="78c71-146">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="78c71-147">Nowe — AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="78c71-147">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)