---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: cdd52b1e1bab28956605d70e1089d7804b8ccff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717358"
---
# <span data-ttu-id="92f3a-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="92f3a-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="92f3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="92f3a-103">Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="92f3a-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92f3a-104">SYNTAX</span></span>

### <span data-ttu-id="92f3a-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="92f3a-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92f3a-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="92f3a-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92f3a-107">Directory</span><span class="sxs-lookup"><span data-stu-id="92f3a-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92f3a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="92f3a-108">DESCRIPTION</span></span>
<span data-ttu-id="92f3a-109">Polecenie cmdlet **Remove-AzureStorageDirectory** Usuwa katalog.</span><span class="sxs-lookup"><span data-stu-id="92f3a-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="92f3a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92f3a-110">EXAMPLES</span></span>

### <span data-ttu-id="92f3a-111">Przykład 1. Usuń folder</span><span class="sxs-lookup"><span data-stu-id="92f3a-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="92f3a-112">To polecenie usuwa folder o nazwie ContosoWorkingFolder z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="92f3a-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="92f3a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92f3a-113">PARAMETERS</span></span>

### <span data-ttu-id="92f3a-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92f3a-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="92f3a-115">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="92f3a-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="92f3a-116">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="92f3a-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="92f3a-117">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="92f3a-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="92f3a-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="92f3a-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="92f3a-119">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="92f3a-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="92f3a-120">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="92f3a-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="92f3a-121">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="92f3a-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="92f3a-122">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="92f3a-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="92f3a-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="92f3a-123">The default value is 10.</span></span>

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

### <span data-ttu-id="92f3a-124">-Context</span><span class="sxs-lookup"><span data-stu-id="92f3a-124">-Context</span></span>
<span data-ttu-id="92f3a-125">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="92f3a-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="92f3a-126">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="92f3a-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="92f3a-127">-Directory</span><span class="sxs-lookup"><span data-stu-id="92f3a-127">-Directory</span></span>
<span data-ttu-id="92f3a-128">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="92f3a-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="92f3a-129">To polecenie cmdlet umożliwia usunięcie folderu, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="92f3a-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="92f3a-130">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="92f3a-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="92f3a-131">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzureStorageFile** .</span><span class="sxs-lookup"><span data-stu-id="92f3a-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92f3a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92f3a-132">-PassThru</span></span>
<span data-ttu-id="92f3a-133">Wskazuje, że jeśli to polecenie cmdlet powiedzie się, zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="92f3a-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="92f3a-134">Jeśli określisz ten parametr, a jeśli polecenie cmdlet nie powiodło się z powodu nieodpowiedniej wartości parametru _Path_ , polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="92f3a-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="92f3a-135">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="92f3a-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="92f3a-136">-Path</span><span class="sxs-lookup"><span data-stu-id="92f3a-136">-Path</span></span>
<span data-ttu-id="92f3a-137">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="92f3a-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="92f3a-138">Jeśli folder, który określi ten parametr, jest pusty, to polecenie cmdlet usuwa ten folder.</span><span class="sxs-lookup"><span data-stu-id="92f3a-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="92f3a-139">Jeśli folder nie jest pusty, to polecenie cmdlet nie zmienia się i zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="92f3a-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f3a-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92f3a-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="92f3a-141">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="92f3a-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="92f3a-142">-Share</span><span class="sxs-lookup"><span data-stu-id="92f3a-142">-Share</span></span>
<span data-ttu-id="92f3a-143">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="92f3a-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="92f3a-144">To polecenie cmdlet usuwa folder w obszarze udział pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="92f3a-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="92f3a-145">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="92f3a-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="92f3a-146">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="92f3a-146">This object contains the storage context.</span></span>
<span data-ttu-id="92f3a-147">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="92f3a-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="92f3a-148">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="92f3a-148">-ShareName</span></span>
<span data-ttu-id="92f3a-149">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="92f3a-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="92f3a-150">To polecenie cmdlet usuwa folder w obszarze udział pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="92f3a-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f3a-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92f3a-151">-Confirm</span></span>
<span data-ttu-id="92f3a-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92f3a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92f3a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92f3a-153">-WhatIf</span></span>
<span data-ttu-id="92f3a-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92f3a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92f3a-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92f3a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92f3a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f3a-156">CommonParameters</span></span>
<span data-ttu-id="92f3a-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f3a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f3a-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f3a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f3a-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92f3a-159">INPUTS</span></span>

### <span data-ttu-id="92f3a-160">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="92f3a-160">IStorageContext</span></span>

<span data-ttu-id="92f3a-161">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="92f3a-161">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="92f3a-162">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="92f3a-162">CloudFileDirectory</span></span>

<span data-ttu-id="92f3a-163">Parametr "katalog" akceptuje wartość typu "CloudFileDirectory" z procesu</span><span class="sxs-lookup"><span data-stu-id="92f3a-163">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="92f3a-164">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="92f3a-164">CloudFileShare</span></span>

<span data-ttu-id="92f3a-165">Parametr "Udostępnij" akceptuje wartość typu "CloudFileShare" z procesu</span><span class="sxs-lookup"><span data-stu-id="92f3a-165">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="92f3a-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92f3a-166">OUTPUTS</span></span>

## <span data-ttu-id="92f3a-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92f3a-167">NOTES</span></span>

## <span data-ttu-id="92f3a-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92f3a-168">RELATED LINKS</span></span>

[<span data-ttu-id="92f3a-169">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="92f3a-169">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="92f3a-170">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="92f3a-170">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="92f3a-171">Nowe — AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="92f3a-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)