---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523549"
---
# <span data-ttu-id="9a7bd-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9a7bd-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="9a7bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7bd-103">Usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-103">Deletes a file share.</span></span>

## <span data-ttu-id="9a7bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a7bd-104">SYNTAX</span></span>

### <span data-ttu-id="9a7bd-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9a7bd-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7bd-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="9a7bd-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a7bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9a7bd-107">DESCRIPTION</span></span>
<span data-ttu-id="9a7bd-108">Polecenie cmdlet **Remove-AzureStorageShare** usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="9a7bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a7bd-109">EXAMPLES</span></span>

### <span data-ttu-id="9a7bd-110">Przykład 1: usuwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="9a7bd-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="9a7bd-111">To polecenie usuwa udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="9a7bd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a7bd-112">PARAMETERS</span></span>

### <span data-ttu-id="9a7bd-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a7bd-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9a7bd-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9a7bd-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9a7bd-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9a7bd-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9a7bd-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9a7bd-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9a7bd-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9a7bd-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9a7bd-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9a7bd-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-122">The default value is 10.</span></span>

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

### <span data-ttu-id="9a7bd-123">-Context</span><span class="sxs-lookup"><span data-stu-id="9a7bd-123">-Context</span></span>
<span data-ttu-id="9a7bd-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9a7bd-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7bd-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7bd-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9a7bd-126">-Force</span></span>
<span data-ttu-id="9a7bd-127">Wymuś usunięcie udziału i całej zawartości</span><span class="sxs-lookup"><span data-stu-id="9a7bd-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="9a7bd-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a7bd-128">-Name</span></span>
<span data-ttu-id="9a7bd-129">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="9a7bd-130">To polecenie cmdlet usuwa udział plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7bd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a7bd-131">-PassThru</span></span>
<span data-ttu-id="9a7bd-132">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9a7bd-133">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9a7bd-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a7bd-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9a7bd-135">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9a7bd-136">-Share</span><span class="sxs-lookup"><span data-stu-id="9a7bd-136">-Share</span></span>
<span data-ttu-id="9a7bd-137">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="9a7bd-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9a7bd-138">To polecenie cmdlet usuwa obiekt, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="9a7bd-139">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="9a7bd-140">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-140">This object contains the storage context.</span></span>
<span data-ttu-id="9a7bd-141">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="9a7bd-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7bd-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a7bd-142">-Confirm</span></span>
<span data-ttu-id="9a7bd-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7bd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7bd-144">-WhatIf</span></span>
<span data-ttu-id="9a7bd-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a7bd-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7bd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7bd-147">CommonParameters</span></span>
<span data-ttu-id="9a7bd-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7bd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7bd-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a7bd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7bd-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a7bd-150">INPUTS</span></span>

## <span data-ttu-id="9a7bd-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a7bd-151">OUTPUTS</span></span>

## <span data-ttu-id="9a7bd-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a7bd-152">NOTES</span></span>

## <span data-ttu-id="9a7bd-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a7bd-153">RELATED LINKS</span></span>

[<span data-ttu-id="9a7bd-154">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9a7bd-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9a7bd-155">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a7bd-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9a7bd-156">Nowe — AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9a7bd-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
