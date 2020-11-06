---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 66662899694f7b1fb93dd109e1dccefee5e00182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552515"
---
# <span data-ttu-id="ff183-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff183-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="ff183-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff183-102">SYNOPSIS</span></span>
<span data-ttu-id="ff183-103">Usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="ff183-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff183-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff183-104">SYNTAX</span></span>

### <span data-ttu-id="ff183-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ff183-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff183-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="ff183-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff183-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff183-107">DESCRIPTION</span></span>
<span data-ttu-id="ff183-108">Polecenie cmdlet **Remove-AzureStorageShare** usuwa udział plików.</span><span class="sxs-lookup"><span data-stu-id="ff183-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="ff183-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff183-109">EXAMPLES</span></span>

### <span data-ttu-id="ff183-110">Przykład 1: usuwanie udziału plików</span><span class="sxs-lookup"><span data-stu-id="ff183-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="ff183-111">To polecenie usuwa udział plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="ff183-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="ff183-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff183-112">PARAMETERS</span></span>

### <span data-ttu-id="ff183-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ff183-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ff183-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="ff183-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ff183-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="ff183-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ff183-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="ff183-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ff183-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ff183-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ff183-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ff183-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ff183-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="ff183-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ff183-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="ff183-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ff183-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="ff183-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ff183-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="ff183-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ff183-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ff183-123">-Context</span></span>
<span data-ttu-id="ff183-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ff183-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff183-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="ff183-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ff183-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ff183-126">-Force</span></span>
<span data-ttu-id="ff183-127">Wymuś usunięcie udziału i całej zawartości</span><span class="sxs-lookup"><span data-stu-id="ff183-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="ff183-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff183-128">-Name</span></span>
<span data-ttu-id="ff183-129">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="ff183-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="ff183-130">To polecenie cmdlet usuwa udział plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ff183-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff183-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff183-131">-PassThru</span></span>
<span data-ttu-id="ff183-132">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="ff183-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ff183-133">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="ff183-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ff183-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ff183-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ff183-135">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="ff183-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ff183-136">-Share</span><span class="sxs-lookup"><span data-stu-id="ff183-136">-Share</span></span>
<span data-ttu-id="ff183-137">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="ff183-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ff183-138">To polecenie cmdlet usuwa obiekt, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ff183-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="ff183-139">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="ff183-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="ff183-140">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="ff183-140">This object contains the storage context.</span></span>
<span data-ttu-id="ff183-141">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="ff183-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="ff183-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff183-142">-Confirm</span></span>
<span data-ttu-id="ff183-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff183-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff183-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff183-144">-WhatIf</span></span>
<span data-ttu-id="ff183-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff183-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff183-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff183-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff183-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff183-147">CommonParameters</span></span>
<span data-ttu-id="ff183-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff183-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff183-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff183-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff183-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff183-150">INPUTS</span></span>

### <span data-ttu-id="ff183-151">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff183-151">IStorageContext</span></span>

<span data-ttu-id="ff183-152">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="ff183-152">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ff183-153">Ciąg</span><span class="sxs-lookup"><span data-stu-id="ff183-153">String</span></span>

<span data-ttu-id="ff183-154">Parametr "nazwa" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="ff183-154">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ff183-155">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ff183-155">CloudFileShare</span></span>

<span data-ttu-id="ff183-156">Parametr "Udostępnij" akceptuje wartość typu "CloudFileShare" z procesu</span><span class="sxs-lookup"><span data-stu-id="ff183-156">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="ff183-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff183-157">OUTPUTS</span></span>

## <span data-ttu-id="ff183-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff183-158">NOTES</span></span>

## <span data-ttu-id="ff183-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff183-159">RELATED LINKS</span></span>

[<span data-ttu-id="ff183-160">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff183-160">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="ff183-161">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff183-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ff183-162">Nowe — AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff183-162">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
