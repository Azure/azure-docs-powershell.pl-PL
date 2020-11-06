---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24b4ddfa86027885b5094b164f24da36e9604900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523545"
---
# <span data-ttu-id="dcd21-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="dcd21-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="dcd21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcd21-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd21-103">Usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="dcd21-103">Deletes a file.</span></span>

## <span data-ttu-id="dcd21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcd21-104">SYNTAX</span></span>

### <span data-ttu-id="dcd21-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="dcd21-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd21-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="dcd21-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd21-107">Directory</span><span class="sxs-lookup"><span data-stu-id="dcd21-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd21-108">Plik</span><span class="sxs-lookup"><span data-stu-id="dcd21-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd21-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dcd21-109">DESCRIPTION</span></span>
<span data-ttu-id="dcd21-110">Polecenie cmdlet **Remove-AzureStorageFile** usuwa plik.</span><span class="sxs-lookup"><span data-stu-id="dcd21-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="dcd21-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcd21-111">EXAMPLES</span></span>

### <span data-ttu-id="dcd21-112">Przykład 1: usuwanie pliku z udziału plików</span><span class="sxs-lookup"><span data-stu-id="dcd21-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="dcd21-113">To polecenie usuwa plik o nazwie ContosoFile22 z udziału plików o nazwie ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="dcd21-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="dcd21-114">Przykład 2: uzyskiwanie pliku z udziału plików za pomocą obiektu udostępniania plików</span><span class="sxs-lookup"><span data-stu-id="dcd21-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="dcd21-115">To polecenie korzysta z polecenia cmdlet **Get-AzureStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie przekazanie tego obiektu do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="dcd21-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dcd21-116">Bieżące polecenie usuwa plik o nazwie ContosoFile22 z ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="dcd21-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="dcd21-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcd21-117">PARAMETERS</span></span>

### <span data-ttu-id="dcd21-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd21-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dcd21-119">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="dcd21-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dcd21-120">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="dcd21-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dcd21-121">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="dcd21-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dcd21-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dcd21-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dcd21-123">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="dcd21-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dcd21-124">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="dcd21-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dcd21-125">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="dcd21-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dcd21-126">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="dcd21-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dcd21-127">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="dcd21-127">The default value is 10.</span></span>

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

### <span data-ttu-id="dcd21-128">-Context</span><span class="sxs-lookup"><span data-stu-id="dcd21-128">-Context</span></span>
<span data-ttu-id="dcd21-129">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="dcd21-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dcd21-130">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="dcd21-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dcd21-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="dcd21-131">-Directory</span></span>
<span data-ttu-id="dcd21-132">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="dcd21-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="dcd21-133">To polecenie cmdlet usuwa plik znajdujący się w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="dcd21-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="dcd21-134">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="dcd21-134">-File</span></span>
<span data-ttu-id="dcd21-135">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="dcd21-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="dcd21-136">To polecenie cmdlet umożliwia usunięcie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="dcd21-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="dcd21-137">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="dcd21-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="dcd21-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcd21-138">-PassThru</span></span>
<span data-ttu-id="dcd21-139">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="dcd21-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="dcd21-140">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="dcd21-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="dcd21-141">-Path</span><span class="sxs-lookup"><span data-stu-id="dcd21-141">-Path</span></span>
<span data-ttu-id="dcd21-142">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="dcd21-142">Specifies the path of a file.</span></span>
<span data-ttu-id="dcd21-143">To polecenie cmdlet usuwa plik, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="dcd21-143">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="dcd21-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd21-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dcd21-145">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="dcd21-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dcd21-146">-Share</span><span class="sxs-lookup"><span data-stu-id="dcd21-146">-Share</span></span>
<span data-ttu-id="dcd21-147">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="dcd21-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="dcd21-148">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="dcd21-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="dcd21-149">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="dcd21-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="dcd21-150">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="dcd21-150">This object contains the storage context.</span></span>
<span data-ttu-id="dcd21-151">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="dcd21-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="dcd21-152">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="dcd21-152">-ShareName</span></span>
<span data-ttu-id="dcd21-153">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="dcd21-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="dcd21-154">To polecenie cmdlet usuwa plik w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="dcd21-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="dcd21-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcd21-155">-Confirm</span></span>
<span data-ttu-id="dcd21-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd21-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd21-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd21-157">-WhatIf</span></span>
<span data-ttu-id="dcd21-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd21-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd21-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dcd21-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd21-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd21-160">CommonParameters</span></span>
<span data-ttu-id="dcd21-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd21-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd21-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd21-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd21-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcd21-163">INPUTS</span></span>

## <span data-ttu-id="dcd21-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcd21-164">OUTPUTS</span></span>

## <span data-ttu-id="dcd21-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcd21-165">NOTES</span></span>

## <span data-ttu-id="dcd21-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcd21-166">RELATED LINKS</span></span>

[<span data-ttu-id="dcd21-167">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="dcd21-167">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="dcd21-168">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd21-168">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="dcd21-169">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dcd21-169">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
