---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 756819d39764fc0d12cd08e0bf0d3edd447cca51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887969"
---
# <span data-ttu-id="9a9b9-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9a9b9-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="9a9b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9b9-103">Umożliwia pobranie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="9a9b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a9b9-104">SYNTAX</span></span>

### <span data-ttu-id="9a9b9-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9a9b9-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="9a9b9-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="9a9b9-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="9a9b9-107">Directory</span><span class="sxs-lookup"><span data-stu-id="9a9b9-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="9a9b9-108">Plik</span><span class="sxs-lookup"><span data-stu-id="9a9b9-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="9a9b9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9a9b9-109">DESCRIPTION</span></span>
<span data-ttu-id="9a9b9-110">Polecenie cmdlet **Get-AzStorageFileContent** pobiera zawartość pliku, a następnie zapisuje je w określonym miejscu docelowym.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="9a9b9-111">To polecenie cmdlet nie zwraca zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="9a9b9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a9b9-112">EXAMPLES</span></span>

### <span data-ttu-id="9a9b9-113">Przykład 1. Pobieranie pliku z folderu</span><span class="sxs-lookup"><span data-stu-id="9a9b9-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="9a9b9-114">To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z folderu udziału pliku ContosoShare06 do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="9a9b9-115">Przykład 2: pobranie plików w obszarze przykładowy udział plików</span><span class="sxs-lookup"><span data-stu-id="9a9b9-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="9a9b9-116">W tym przykładzie udostępniono pliki w obszarze przykładowego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="9a9b9-117">Przykład 3: Pobierz plik platformy Azure do pliku lokalnego, a perserve właściwości SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="9a9b9-118">W tym przykładzie plik usługi Azure jest pobierany do pliku lokalnego, a perserves właściwości SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="9a9b9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a9b9-119">PARAMETERS</span></span>

### <span data-ttu-id="9a9b9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a9b9-120">-AsJob</span></span>
<span data-ttu-id="9a9b9-121">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-121">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="9a9b9-122">-CheckMd5</span></span>
<span data-ttu-id="9a9b9-123">Określa, czy ma być sprawdzana suma Md5 dla pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a9b9-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9a9b9-125">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="9a9b9-126">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="9a9b9-127">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9a9b9-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9a9b9-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9a9b9-129">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="9a9b9-130">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="9a9b9-131">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="9a9b9-132">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="9a9b9-133">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-133">The default value is 10.</span></span>

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

### <span data-ttu-id="9a9b9-134">-Context</span><span class="sxs-lookup"><span data-stu-id="9a9b9-134">-Context</span></span>
<span data-ttu-id="9a9b9-135">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="9a9b9-136">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9a9b9-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a9b9-137">-DefaultProfile</span></span>
<span data-ttu-id="9a9b9-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a9b9-139">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="9a9b9-139">-Destination</span></span>
<span data-ttu-id="9a9b9-140">Określa ścieżkę docelową.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-140">Specifies the destination path.</span></span>
<span data-ttu-id="9a9b9-141">To polecenie cmdlet pobiera zawartość pliku do lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="9a9b9-142">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9a9b9-143">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9a9b9-144">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-144">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="9a9b9-145">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="9a9b9-146">-Directory</span></span>
<span data-ttu-id="9a9b9-147">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="9a9b9-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9a9b9-148">To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="9a9b9-149">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="9a9b9-150">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="9a9b9-151">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="9a9b9-151">-File</span></span>
<span data-ttu-id="9a9b9-152">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="9a9b9-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="9a9b9-153">To polecenie cmdlet umożliwia pobieranie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="9a9b9-154">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-155">-Force</span><span class="sxs-lookup"><span data-stu-id="9a9b9-155">-Force</span></span>
<span data-ttu-id="9a9b9-156">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9a9b9-157">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9a9b9-158">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-158">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="9a9b9-159">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a9b9-160">-PassThru</span></span>
<span data-ttu-id="9a9b9-161">Wskazuje, że to polecenie cmdlet zwróci obiekt **AzureStorageFile** , który jest przez niego pobierany.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-162">-Path</span><span class="sxs-lookup"><span data-stu-id="9a9b9-162">-Path</span></span>
<span data-ttu-id="9a9b9-163">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-163">Specifies the path of a file.</span></span>
<span data-ttu-id="9a9b9-164">Ten aplet polecenia pobiera zawartość pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="9a9b9-165">Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="9a9b9-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="9a9b9-167">Zachowanie właściwości pliku źródłowego SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku docelowym.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="9a9b9-168">Ten parametr jest dostępny tylko w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-168">This parameter is only available on Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a9b9-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9a9b9-170">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="9a9b9-171">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9a9b9-172">-Share</span><span class="sxs-lookup"><span data-stu-id="9a9b9-172">-Share</span></span>
<span data-ttu-id="9a9b9-173">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="9a9b9-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9a9b9-174">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="9a9b9-175">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="9a9b9-176">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-176">This object contains the storage context.</span></span>
<span data-ttu-id="9a9b9-177">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="9a9b9-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9a9b9-178">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="9a9b9-178">-ShareName</span></span>
<span data-ttu-id="9a9b9-179">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="9a9b9-180">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="9a9b9-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a9b9-181">-Confirm</span></span>
<span data-ttu-id="9a9b9-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a9b9-183">-WhatIf</span></span>
<span data-ttu-id="9a9b9-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a9b9-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9b9-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9b9-186">CommonParameters</span></span>
<span data-ttu-id="9a9b9-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9b9-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a9b9-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9b9-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a9b9-189">INPUTS</span></span>

### <span data-ttu-id="9a9b9-190">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9a9b9-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9a9b9-191">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9a9b9-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9a9b9-192">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="9a9b9-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="9a9b9-193">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a9b9-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9a9b9-194">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a9b9-194">OUTPUTS</span></span>

### <span data-ttu-id="9a9b9-195">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="9a9b9-195">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="9a9b9-196">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a9b9-196">NOTES</span></span>

## <span data-ttu-id="9a9b9-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a9b9-197">RELATED LINKS</span></span>

[<span data-ttu-id="9a9b9-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="9a9b9-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="9a9b9-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9a9b9-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


