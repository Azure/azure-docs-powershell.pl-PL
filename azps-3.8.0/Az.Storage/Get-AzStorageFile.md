---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: aadbbbaaefe1090b221e049d310bf262fdddf28c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050198"
---
# <span data-ttu-id="756c4-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="756c4-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="756c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="756c4-102">SYNOPSIS</span></span>
<span data-ttu-id="756c4-103">Wyświetla listę katalogów i plików ścieżki.</span><span class="sxs-lookup"><span data-stu-id="756c4-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="756c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="756c4-104">SYNTAX</span></span>

### <span data-ttu-id="756c4-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="756c4-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="756c4-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="756c4-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="756c4-107">Directory</span><span class="sxs-lookup"><span data-stu-id="756c4-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="756c4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="756c4-108">DESCRIPTION</span></span>
<span data-ttu-id="756c4-109">Polecenie cmdlet **Get-AzStorageFile** zawiera listę katalogów i plików dla określonego udziału lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="756c4-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="756c4-110">Określ parametr *Path* , aby uzyskać wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="756c4-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="756c4-111">To polecenie cmdlet zwraca obiekty **AzureStorageFile** i **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="756c4-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="756c4-112">Właściwości **IsDirectory** można użyć w celu rozróżnienia folderów i plików.</span><span class="sxs-lookup"><span data-stu-id="756c4-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="756c4-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="756c4-113">EXAMPLES</span></span>

### <span data-ttu-id="756c4-114">Przykład 1: Wyświetlanie listy katalogów w udziale</span><span class="sxs-lookup"><span data-stu-id="756c4-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="756c4-115">To polecenie wyświetla listę tylko katalogów w ContosoShare06 udostępniania.</span><span class="sxs-lookup"><span data-stu-id="756c4-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="756c4-116">Po pierwsze pobiera zarówno pliki, jak i katalogi, przekazuje je operatorowi **WHERE** za pomocą operatora potoku, a następnie odrzuca wszystkie obiekty, których typ nie jest "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="756c4-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="756c4-117">Przykład 2: wyświetlanie katalogu plików</span><span class="sxs-lookup"><span data-stu-id="756c4-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="756c4-118">To polecenie wyświetla listę plików i folderów w katalogu ContosoWorkingFolder w obszarze Udostępnij ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="756c4-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="756c4-119">Najpierw otrzymuje ono wystąpienie katalogu, a następnie przejdzie do polecenia cmdlet **Get-AzStorageFile** w celu utworzenia listy katalogów.</span><span class="sxs-lookup"><span data-stu-id="756c4-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="756c4-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="756c4-120">PARAMETERS</span></span>

### <span data-ttu-id="756c4-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="756c4-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="756c4-122">Określa interwał limitu czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="756c4-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="756c4-123">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wysłania żądania.</span><span class="sxs-lookup"><span data-stu-id="756c4-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="756c4-124">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="756c4-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="756c4-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="756c4-126">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="756c4-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="756c4-127">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="756c4-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="756c4-128">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="756c4-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="756c4-129">Ten parametr może pomóc w ograniczeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="756c4-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="756c4-130">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="756c4-130">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-131">-Context</span><span class="sxs-lookup"><span data-stu-id="756c4-131">-Context</span></span>
<span data-ttu-id="756c4-132">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="756c4-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="756c4-133">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="756c4-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756c4-134">-DefaultProfile</span></span>
<span data-ttu-id="756c4-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="756c4-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="756c4-136">-Directory</span></span>
<span data-ttu-id="756c4-137">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="756c4-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="756c4-138">To polecenie cmdlet spowoduje wyświetlenie folderu, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="756c4-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="756c4-139">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="756c4-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="756c4-140">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzStorageFile** .</span><span class="sxs-lookup"><span data-stu-id="756c4-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-141">-Path</span><span class="sxs-lookup"><span data-stu-id="756c4-141">-Path</span></span>
<span data-ttu-id="756c4-142">Określa ścieżkę do folderu.</span><span class="sxs-lookup"><span data-stu-id="756c4-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="756c4-143">W przypadku pominięcia parametru *Path* polecenie **Get-AzStorageFile** wyświetla listę katalogów i plików w określonym udziale plików lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="756c4-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="756c4-144">Jeśli dołączasz parametr *Path* , funkcja **Get-AzStorageFile** zwraca wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="756c4-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="756c4-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="756c4-146">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="756c4-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="756c4-147">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="756c4-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-148">-Share</span><span class="sxs-lookup"><span data-stu-id="756c4-148">-Share</span></span>
<span data-ttu-id="756c4-149">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="756c4-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="756c4-150">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="756c4-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="756c4-151">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="756c4-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="756c4-152">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="756c4-152">This object contains the Storage context.</span></span>
<span data-ttu-id="756c4-153">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="756c4-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-154">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="756c4-154">-ShareName</span></span>
<span data-ttu-id="756c4-155">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="756c4-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="756c4-156">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="756c4-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756c4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756c4-157">CommonParameters</span></span>
<span data-ttu-id="756c4-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="756c4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756c4-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="756c4-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756c4-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="756c4-160">INPUTS</span></span>

### <span data-ttu-id="756c4-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="756c4-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="756c4-162">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="756c4-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="756c4-163">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="756c4-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="756c4-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="756c4-164">OUTPUTS</span></span>

### <span data-ttu-id="756c4-165">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="756c4-165">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="756c4-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="756c4-166">NOTES</span></span>

## <span data-ttu-id="756c4-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="756c4-167">RELATED LINKS</span></span>

[<span data-ttu-id="756c4-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="756c4-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="756c4-169">Nowe — AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="756c4-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="756c4-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="756c4-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="756c4-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="756c4-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="756c4-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="756c4-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


