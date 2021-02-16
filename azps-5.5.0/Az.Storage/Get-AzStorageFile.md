---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197563"
---
# <span data-ttu-id="fa40b-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="fa40b-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="fa40b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa40b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa40b-103">Lista katalogów i plików dla ścieżki.</span><span class="sxs-lookup"><span data-stu-id="fa40b-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="fa40b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa40b-104">SYNTAX</span></span>

### <span data-ttu-id="fa40b-105">ShareName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="fa40b-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fa40b-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="fa40b-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa40b-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="fa40b-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa40b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa40b-108">DESCRIPTION</span></span>
<span data-ttu-id="fa40b-109">Polecenie **cmdlet Get-AzStorageFile** zawiera listę katalogów i plików dla określonego przez Ciebie udziału lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="fa40b-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="fa40b-110">Określ parametr *Ścieżka,* aby uzyskać wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="fa40b-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="fa40b-111">To polecenie cmdlet zwraca **obiekty AzureStorageFile** i **AzureStorageDirectory.**</span><span class="sxs-lookup"><span data-stu-id="fa40b-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="fa40b-112">Właściwość **IsDirectory** umożliwia rozróżnienie folderów i plików.</span><span class="sxs-lookup"><span data-stu-id="fa40b-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="fa40b-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa40b-113">EXAMPLES</span></span>

### <span data-ttu-id="fa40b-114">Przykład 1. Lista katalogów w udostępniniu</span><span class="sxs-lookup"><span data-stu-id="fa40b-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="fa40b-115">To polecenie wyświetla listę tylko katalogów w użytce ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fa40b-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="fa40b-116">Najpierw pobiera zarówno pliki, jak i katalogi, przekazuje je do operatora **where** przy użyciu operatora potoku, a następnie odrzuca wszystkie obiekty o typie innym niż "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="fa40b-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="fa40b-117">Przykład 2. Lista katalogu plików</span><span class="sxs-lookup"><span data-stu-id="fa40b-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="fa40b-118">To polecenie zawiera listę plików i folderów w katalogu ContosoWorkingFolder w ramach udziału ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fa40b-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="fa40b-119">Najpierw pobiera wystąpienie katalogu, a następnie potokuje je do polecenia cmdlet **Get-AzStorageFile,** aby wyświetlić listę katalogu.</span><span class="sxs-lookup"><span data-stu-id="fa40b-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="fa40b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa40b-120">PARAMETERS</span></span>

### <span data-ttu-id="fa40b-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa40b-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fa40b-122">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="fa40b-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fa40b-123">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="fa40b-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fa40b-124">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="fa40b-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fa40b-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fa40b-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fa40b-126">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fa40b-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fa40b-127">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="fa40b-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fa40b-128">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="fa40b-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fa40b-129">Ten parametr może pomóc zminimalizować problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="fa40b-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fa40b-130">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="fa40b-130">The default value is 10.</span></span>

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

### <span data-ttu-id="fa40b-131">— kontekst</span><span class="sxs-lookup"><span data-stu-id="fa40b-131">-Context</span></span>
<span data-ttu-id="fa40b-132">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa40b-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="fa40b-133">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa40b-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fa40b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa40b-134">-DefaultProfile</span></span>
<span data-ttu-id="fa40b-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa40b-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa40b-136">— Katalog</span><span class="sxs-lookup"><span data-stu-id="fa40b-136">-Directory</span></span>
<span data-ttu-id="fa40b-137">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="fa40b-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="fa40b-138">To polecenie cmdlet pobiera folder, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fa40b-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="fa40b-139">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa40b-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="fa40b-140">Aby uzyskać katalog, możesz również użyć polecenia cmdlet **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="fa40b-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="fa40b-141">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="fa40b-141">-Path</span></span>
<span data-ttu-id="fa40b-142">Określa ścieżkę folderu.</span><span class="sxs-lookup"><span data-stu-id="fa40b-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="fa40b-143">Jeśli parametr Path zostanie *pominięty,* plik **Get-AzStorageFile** będzie zawierał listę katalogów i plików w określonym udziału plików lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="fa40b-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="fa40b-144">Jeśli uwzględnisz parametr *Path,* **funkcja Get-AzStorageFile** zwróci wystąpienie katalogu lub pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="fa40b-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="fa40b-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa40b-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fa40b-146">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="fa40b-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="fa40b-147">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="fa40b-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="fa40b-148">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="fa40b-148">-Share</span></span>
<span data-ttu-id="fa40b-149">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="fa40b-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fa40b-150">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fa40b-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="fa40b-151">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa40b-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="fa40b-152">Ten obiekt zawiera kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa40b-152">This object contains the Storage context.</span></span>
<span data-ttu-id="fa40b-153">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="fa40b-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fa40b-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fa40b-154">-ShareName</span></span>
<span data-ttu-id="fa40b-155">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="fa40b-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="fa40b-156">To polecenie cmdlet pobiera plik lub katalog z udziału plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fa40b-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa40b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa40b-157">CommonParameters</span></span>
<span data-ttu-id="fa40b-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa40b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa40b-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa40b-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa40b-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa40b-160">INPUTS</span></span>

### <span data-ttu-id="fa40b-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="fa40b-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="fa40b-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="fa40b-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="fa40b-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa40b-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fa40b-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa40b-164">OUTPUTS</span></span>

### <span data-ttu-id="fa40b-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="fa40b-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="fa40b-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa40b-166">NOTES</span></span>

## <span data-ttu-id="fa40b-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa40b-167">RELATED LINKS</span></span>

[<span data-ttu-id="fa40b-168">Get-AzstorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fa40b-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="fa40b-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="fa40b-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="fa40b-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="fa40b-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="fa40b-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="fa40b-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="fa40b-172">Set-azstorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fa40b-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


