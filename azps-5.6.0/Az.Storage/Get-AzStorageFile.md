---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: e61171faba3661ad1d518641655ad87f06771ae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997095"
---
# <span data-ttu-id="d02eb-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d02eb-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="d02eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d02eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d02eb-103">Lista katalogów i plików dla ścieżki.</span><span class="sxs-lookup"><span data-stu-id="d02eb-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="d02eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d02eb-104">SYNTAX</span></span>

### <span data-ttu-id="d02eb-105">ShareName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d02eb-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d02eb-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="d02eb-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="d02eb-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="d02eb-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="d02eb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d02eb-108">DESCRIPTION</span></span>
<span data-ttu-id="d02eb-109">Polecenie **cmdlet Get-AzStorageFile** zawiera listę katalogów i plików dla owego udziału lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="d02eb-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="d02eb-110">Określ parametr *Ścieżka,* aby uzyskać wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="d02eb-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="d02eb-111">To polecenie cmdlet zwraca **obiekty AzureStorageFile** i **AzureStorageDirectory.**</span><span class="sxs-lookup"><span data-stu-id="d02eb-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="d02eb-112">Właściwość **IsDirectory** umożliwia rozróżnienie folderów i plików.</span><span class="sxs-lookup"><span data-stu-id="d02eb-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="d02eb-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d02eb-113">EXAMPLES</span></span>

### <span data-ttu-id="d02eb-114">Przykład 1. Lista katalogów w udostępniniu</span><span class="sxs-lookup"><span data-stu-id="d02eb-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="d02eb-115">To polecenie wyświetla listę tylko katalogów w użytce ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="d02eb-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="d02eb-116">Najpierw pobiera zarówno pliki, jak i katalogi, przekazuje je do operatora **where** przy użyciu operatora potoku, a następnie odrzuca wszystkie obiekty o typie innym niż "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="d02eb-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="d02eb-117">Przykład 2. Lista katalogu plików</span><span class="sxs-lookup"><span data-stu-id="d02eb-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="d02eb-118">To polecenie zawiera listę plików i folderów w katalogu ContosoWorkingFolder w ramach udziału ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="d02eb-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="d02eb-119">Najpierw pobiera wystąpienie katalogu, a następnie potokuje je do polecenia cmdlet **Get-AzStorageFile,** aby wyświetlić katalog.</span><span class="sxs-lookup"><span data-stu-id="d02eb-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="d02eb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d02eb-120">PARAMETERS</span></span>

### <span data-ttu-id="d02eb-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d02eb-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d02eb-122">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="d02eb-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d02eb-123">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="d02eb-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d02eb-124">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="d02eb-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d02eb-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d02eb-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d02eb-126">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="d02eb-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d02eb-127">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="d02eb-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d02eb-128">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="d02eb-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d02eb-129">Ten parametr może pomóc zminimalizować problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="d02eb-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d02eb-130">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="d02eb-130">The default value is 10.</span></span>

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

### <span data-ttu-id="d02eb-131">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d02eb-131">-Context</span></span>
<span data-ttu-id="d02eb-132">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d02eb-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d02eb-133">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d02eb-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d02eb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d02eb-134">-DefaultProfile</span></span>
<span data-ttu-id="d02eb-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d02eb-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d02eb-136">— Katalog</span><span class="sxs-lookup"><span data-stu-id="d02eb-136">-Directory</span></span>
<span data-ttu-id="d02eb-137">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="d02eb-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d02eb-138">To polecenie cmdlet pobiera folder, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d02eb-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="d02eb-139">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d02eb-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d02eb-140">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="d02eb-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d02eb-141">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d02eb-141">-Path</span></span>
<span data-ttu-id="d02eb-142">Określa ścieżkę folderu.</span><span class="sxs-lookup"><span data-stu-id="d02eb-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="d02eb-143">Jeśli parametr Path zostanie *pominięty,* plik **Get-AzStorageFile** będzie zawierał listę katalogów i plików w określonym udziału plików lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="d02eb-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="d02eb-144">Jeśli parametr Path *zostanie* podany, funkcja **Get-AzStorageFile** zwróci wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="d02eb-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="d02eb-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d02eb-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d02eb-146">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="d02eb-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="d02eb-147">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="d02eb-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="d02eb-148">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="d02eb-148">-Share</span></span>
<span data-ttu-id="d02eb-149">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="d02eb-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d02eb-150">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d02eb-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="d02eb-151">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d02eb-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="d02eb-152">Ten obiekt zawiera kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="d02eb-152">This object contains the Storage context.</span></span>
<span data-ttu-id="d02eb-153">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="d02eb-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d02eb-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d02eb-154">-ShareName</span></span>
<span data-ttu-id="d02eb-155">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="d02eb-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="d02eb-156">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d02eb-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="d02eb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d02eb-157">CommonParameters</span></span>
<span data-ttu-id="d02eb-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d02eb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d02eb-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d02eb-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d02eb-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d02eb-160">INPUTS</span></span>

### <span data-ttu-id="d02eb-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="d02eb-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="d02eb-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="d02eb-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="d02eb-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d02eb-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d02eb-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d02eb-164">OUTPUTS</span></span>

### <span data-ttu-id="d02eb-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="d02eb-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="d02eb-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d02eb-166">NOTES</span></span>

## <span data-ttu-id="d02eb-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d02eb-167">RELATED LINKS</span></span>

[<span data-ttu-id="d02eb-168">Get-AzstorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d02eb-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="d02eb-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d02eb-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="d02eb-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d02eb-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="d02eb-171">Remove-azstorageFile</span><span class="sxs-lookup"><span data-stu-id="d02eb-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="d02eb-172">Set-azstorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d02eb-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


