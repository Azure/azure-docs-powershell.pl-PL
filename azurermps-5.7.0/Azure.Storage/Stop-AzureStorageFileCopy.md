---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
ms.openlocfilehash: ea9902b9bf678ad8f914104022a5ce5a7d04eb07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549032"
---
# <span data-ttu-id="8d884-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d884-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="8d884-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d884-102">SYNOPSIS</span></span>
<span data-ttu-id="8d884-103">Zatrzymuje operację kopiowania w określonym pliku docelowym.</span><span class="sxs-lookup"><span data-stu-id="8d884-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d884-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d884-104">SYNTAX</span></span>

### <span data-ttu-id="8d884-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="8d884-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d884-106">Plik</span><span class="sxs-lookup"><span data-stu-id="8d884-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d884-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8d884-107">DESCRIPTION</span></span>
<span data-ttu-id="8d884-108">Polecenie cmdlet **stop-AzureStorageFileCopy** zatrzymuje kopiowanie pliku do pliku docelowego.</span><span class="sxs-lookup"><span data-stu-id="8d884-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="8d884-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d884-109">EXAMPLES</span></span>

### <span data-ttu-id="8d884-110">Przykład 1: zatrzymanie operacji kopiowania</span><span class="sxs-lookup"><span data-stu-id="8d884-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="8d884-111">To polecenie zatrzymuje kopiowanie pliku o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="8d884-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="8d884-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d884-112">PARAMETERS</span></span>

### <span data-ttu-id="8d884-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d884-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8d884-114">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="8d884-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8d884-115">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="8d884-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8d884-116">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="8d884-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8d884-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8d884-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8d884-118">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8d884-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8d884-119">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8d884-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8d884-120">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="8d884-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8d884-121">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="8d884-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8d884-122">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8d884-122">The default value is 10.</span></span>

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

### <span data-ttu-id="8d884-123">-Context</span><span class="sxs-lookup"><span data-stu-id="8d884-123">-Context</span></span>
<span data-ttu-id="8d884-124">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8d884-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d884-125">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8d884-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8d884-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="8d884-126">-CopyId</span></span>
<span data-ttu-id="8d884-127">Określa identyfikator operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="8d884-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d884-128">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="8d884-128">-File</span></span>
<span data-ttu-id="8d884-129">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="8d884-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="8d884-130">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="8d884-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d884-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8d884-131">-FilePath</span></span>
<span data-ttu-id="8d884-132">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="8d884-132">Specifies the path of a file.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d884-133">-Force</span><span class="sxs-lookup"><span data-stu-id="8d884-133">-Force</span></span>
<span data-ttu-id="8d884-134">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8d884-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d884-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d884-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8d884-136">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="8d884-136">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8d884-137">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="8d884-137">-ShareName</span></span>
<span data-ttu-id="8d884-138">Określa nazwę udziału.</span><span class="sxs-lookup"><span data-stu-id="8d884-138">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="8d884-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d884-139">-Confirm</span></span>
<span data-ttu-id="8d884-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d884-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d884-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d884-141">-WhatIf</span></span>
<span data-ttu-id="8d884-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d884-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d884-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d884-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d884-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d884-144">CommonParameters</span></span>
<span data-ttu-id="8d884-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d884-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d884-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d884-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d884-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d884-147">INPUTS</span></span>

### <span data-ttu-id="8d884-148">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d884-148">IStorageContext</span></span>

<span data-ttu-id="8d884-149">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="8d884-149">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8d884-150">CloudFile</span><span class="sxs-lookup"><span data-stu-id="8d884-150">CloudFile</span></span>

<span data-ttu-id="8d884-151">Parametr "File" przyjmuje wartość typu "CloudFile" z procesu</span><span class="sxs-lookup"><span data-stu-id="8d884-151">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="8d884-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d884-152">OUTPUTS</span></span>

## <span data-ttu-id="8d884-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d884-153">NOTES</span></span>

## <span data-ttu-id="8d884-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d884-154">RELATED LINKS</span></span>

[<span data-ttu-id="8d884-155">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8d884-155">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="8d884-156">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="8d884-156">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="8d884-157">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d884-157">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8d884-158">Start — AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d884-158">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
