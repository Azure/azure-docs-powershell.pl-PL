---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524033"
---
# <span data-ttu-id="03661-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="03661-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="03661-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03661-102">SYNOPSIS</span></span>
<span data-ttu-id="03661-103">Wyświetla listę katalogów i plików ścieżki.</span><span class="sxs-lookup"><span data-stu-id="03661-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="03661-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03661-104">SYNTAX</span></span>

### <span data-ttu-id="03661-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="03661-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="03661-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="03661-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="03661-107">Directory</span><span class="sxs-lookup"><span data-stu-id="03661-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="03661-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03661-108">DESCRIPTION</span></span>
<span data-ttu-id="03661-109">Polecenie cmdlet **Get-AzureStorageFile** zawiera listę katalogów i plików dla określonego udziału lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="03661-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="03661-110">Określ parametr *Path* , aby uzyskać wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="03661-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="03661-111">To polecenie cmdlet zwraca obiekty **AzureStorageFile** i **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="03661-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="03661-112">Właściwości **IsDirectory** można użyć w celu rozróżnienia folderów i plików.</span><span class="sxs-lookup"><span data-stu-id="03661-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="03661-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03661-113">EXAMPLES</span></span>

### <span data-ttu-id="03661-114">Przykład 1: Wyświetlanie listy katalogów w udziale</span><span class="sxs-lookup"><span data-stu-id="03661-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="03661-115">To polecenie wyświetla listę tylko katalogów w ContosoShare06 udostępniania.</span><span class="sxs-lookup"><span data-stu-id="03661-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="03661-116">Po pierwsze pobiera zarówno pliki, jak i katalogi, przekazuje je operatorowi **WHERE** za pomocą operatora potoku, a następnie odrzuca wszystkie obiekty, których typ nie jest "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="03661-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="03661-117">Przykład 2: wyświetlanie katalogu plików</span><span class="sxs-lookup"><span data-stu-id="03661-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="03661-118">To polecenie wyświetla listę plików i folderów w katalogu ContosoWorkingFolder w obszarze Udostępnij ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="03661-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="03661-119">Najpierw otrzymuje ono wystąpienie katalogu, a następnie przejdzie do polecenia cmdlet **Get-AzureStorageFile** w celu utworzenia listy katalogów.</span><span class="sxs-lookup"><span data-stu-id="03661-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="03661-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03661-120">PARAMETERS</span></span>

### <span data-ttu-id="03661-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03661-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="03661-122">Określa interwał limitu czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="03661-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="03661-123">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wysłania żądania.</span><span class="sxs-lookup"><span data-stu-id="03661-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="03661-124">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="03661-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="03661-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="03661-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="03661-126">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="03661-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="03661-127">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="03661-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="03661-128">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="03661-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="03661-129">Ten parametr może pomóc w ograniczeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="03661-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="03661-130">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="03661-130">The default value is 10.</span></span>

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

### <span data-ttu-id="03661-131">-Context</span><span class="sxs-lookup"><span data-stu-id="03661-131">-Context</span></span>
<span data-ttu-id="03661-132">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="03661-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="03661-133">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="03661-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03661-134">-Directory</span><span class="sxs-lookup"><span data-stu-id="03661-134">-Directory</span></span>
<span data-ttu-id="03661-135">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="03661-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="03661-136">To polecenie cmdlet spowoduje wyświetlenie folderu, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="03661-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="03661-137">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="03661-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="03661-138">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzureStorageFile** .</span><span class="sxs-lookup"><span data-stu-id="03661-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="03661-139">-Path</span><span class="sxs-lookup"><span data-stu-id="03661-139">-Path</span></span>
<span data-ttu-id="03661-140">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="03661-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="03661-141">W przypadku pominięcia parametru *Path* polecenie **Get-AzureStorageFile** wyświetla listę katalogów i plików w określonym udziale plików lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="03661-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="03661-142">Jeśli dołączasz parametr *Path* , funkcja **Get-AzureStorageFile** zwraca wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="03661-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03661-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03661-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="03661-144">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="03661-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="03661-145">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="03661-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="03661-146">-Share</span><span class="sxs-lookup"><span data-stu-id="03661-146">-Share</span></span>
<span data-ttu-id="03661-147">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="03661-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="03661-148">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="03661-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="03661-149">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="03661-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="03661-150">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="03661-150">This object contains the Storage context.</span></span>
<span data-ttu-id="03661-151">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="03661-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="03661-152">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="03661-152">-ShareName</span></span>
<span data-ttu-id="03661-153">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="03661-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="03661-154">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="03661-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="03661-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03661-155">CommonParameters</span></span>
<span data-ttu-id="03661-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03661-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03661-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03661-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03661-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03661-158">INPUTS</span></span>

## <span data-ttu-id="03661-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03661-159">OUTPUTS</span></span>

## <span data-ttu-id="03661-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03661-160">NOTES</span></span>

## <span data-ttu-id="03661-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03661-161">RELATED LINKS</span></span>

[<span data-ttu-id="03661-162">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="03661-162">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="03661-163">Nowe — AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="03661-163">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="03661-164">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="03661-164">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="03661-165">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="03661-165">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="03661-166">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="03661-166">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


