---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
ms.openlocfilehash: 9055f447093a0e10242824e1e2381523e0b0e81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549815"
---
# <span data-ttu-id="1c8af-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1c8af-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="1c8af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c8af-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8af-103">Usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="1c8af-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c8af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c8af-104">SYNTAX</span></span>

### <span data-ttu-id="1c8af-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1c8af-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c8af-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="1c8af-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c8af-107">Directory</span><span class="sxs-lookup"><span data-stu-id="1c8af-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c8af-108">Plik</span><span class="sxs-lookup"><span data-stu-id="1c8af-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c8af-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1c8af-109">DESCRIPTION</span></span>
<span data-ttu-id="1c8af-110">Polecenie cmdlet **Remove-AzureStorageFile** usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="1c8af-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="1c8af-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c8af-111">EXAMPLES</span></span>

### <span data-ttu-id="1c8af-112">Przykład 1: usuwanie pliku z udziału plików</span><span class="sxs-lookup"><span data-stu-id="1c8af-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="1c8af-113">To polecenie usuwa plik o nazwie ContosoFile22 z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="1c8af-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="1c8af-114">Przykład 2: uzyskiwanie pliku z udziału plików za pomocą obiektu udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="1c8af-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="1c8af-115">To polecenie korzysta z polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie tego obiektu do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1c8af-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1c8af-116">Bieżące polecenie usuwa plik o nazwie ContosoFile22 z ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="1c8af-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="1c8af-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c8af-117">PARAMETERS</span></span>

### <span data-ttu-id="1c8af-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1c8af-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1c8af-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="1c8af-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1c8af-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="1c8af-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1c8af-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="1c8af-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1c8af-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1c8af-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1c8af-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1c8af-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1c8af-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1c8af-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1c8af-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="1c8af-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1c8af-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="1c8af-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1c8af-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="1c8af-127">The default value is 10.</span></span>

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

### <span data-ttu-id="1c8af-128">-Context</span><span class="sxs-lookup"><span data-stu-id="1c8af-128">-Context</span></span>
<span data-ttu-id="1c8af-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1c8af-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1c8af-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8af-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1c8af-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="1c8af-131">-Directory</span></span>
<span data-ttu-id="1c8af-132">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="1c8af-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1c8af-133">To polecenie cmdlet usuwa plik znajdujący się w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1c8af-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c8af-134">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="1c8af-134">-File</span></span>
<span data-ttu-id="1c8af-135">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="1c8af-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="1c8af-136">To polecenie cmdlet umożliwia usunięcie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1c8af-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="1c8af-137">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="1c8af-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1c8af-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c8af-138">-PassThru</span></span>
<span data-ttu-id="1c8af-139">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="1c8af-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1c8af-140">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="1c8af-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1c8af-141">-Path</span><span class="sxs-lookup"><span data-stu-id="1c8af-141">-Path</span></span>
<span data-ttu-id="1c8af-142">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="1c8af-142">Specifies the path of a file.</span></span>
<span data-ttu-id="1c8af-143">To polecenie cmdlet usuwa plik, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1c8af-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8af-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1c8af-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1c8af-145">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="1c8af-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1c8af-146">-Share</span><span class="sxs-lookup"><span data-stu-id="1c8af-146">-Share</span></span>
<span data-ttu-id="1c8af-147">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="1c8af-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1c8af-148">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1c8af-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="1c8af-149">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="1c8af-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="1c8af-150">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1c8af-150">This object contains the storage context.</span></span>
<span data-ttu-id="1c8af-151">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="1c8af-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="1c8af-152">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="1c8af-152">-ShareName</span></span>
<span data-ttu-id="1c8af-153">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="1c8af-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="1c8af-154">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1c8af-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="1c8af-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c8af-155">-Confirm</span></span>
<span data-ttu-id="1c8af-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c8af-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c8af-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c8af-157">-WhatIf</span></span>
<span data-ttu-id="1c8af-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c8af-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c8af-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c8af-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c8af-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8af-160">CommonParameters</span></span>
<span data-ttu-id="1c8af-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c8af-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8af-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c8af-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8af-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c8af-163">INPUTS</span></span>

### <span data-ttu-id="1c8af-164">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c8af-164">IStorageContext</span></span>

<span data-ttu-id="1c8af-165">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="1c8af-165">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1c8af-166">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="1c8af-166">CloudFileDirectory</span></span>

<span data-ttu-id="1c8af-167">Parametr "katalog" akceptuje wartość typu "CloudFileDirectory" z procesu</span><span class="sxs-lookup"><span data-stu-id="1c8af-167">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="1c8af-168">CloudFile</span><span class="sxs-lookup"><span data-stu-id="1c8af-168">CloudFile</span></span>

<span data-ttu-id="1c8af-169">Parametr "File" przyjmuje wartość typu "CloudFile" z procesu</span><span class="sxs-lookup"><span data-stu-id="1c8af-169">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="1c8af-170">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1c8af-170">CloudFileShare</span></span>

<span data-ttu-id="1c8af-171">Parametr "Udostępnij" akceptuje wartość typu "CloudFileShare" z procesu</span><span class="sxs-lookup"><span data-stu-id="1c8af-171">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="1c8af-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c8af-172">OUTPUTS</span></span>

## <span data-ttu-id="1c8af-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c8af-173">NOTES</span></span>

## <span data-ttu-id="1c8af-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c8af-174">RELATED LINKS</span></span>

[<span data-ttu-id="1c8af-175">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1c8af-175">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="1c8af-176">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="1c8af-176">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="1c8af-177">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c8af-177">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
