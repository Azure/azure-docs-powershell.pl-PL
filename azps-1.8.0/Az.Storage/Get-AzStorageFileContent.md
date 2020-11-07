---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 0777c24aa5cb9b505ffc3495c9a9220da912f055
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707625"
---
# <span data-ttu-id="6868c-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6868c-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="6868c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6868c-102">SYNOPSIS</span></span>
<span data-ttu-id="6868c-103">Umożliwia pobranie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="6868c-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="6868c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6868c-104">SYNTAX</span></span>

### <span data-ttu-id="6868c-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6868c-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6868c-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="6868c-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6868c-107">Directory</span><span class="sxs-lookup"><span data-stu-id="6868c-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6868c-108">Plik</span><span class="sxs-lookup"><span data-stu-id="6868c-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6868c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6868c-109">DESCRIPTION</span></span>
<span data-ttu-id="6868c-110">Polecenie cmdlet **Get-AzStorageFileContent** pobiera zawartość pliku, a następnie zapisuje je w określonym miejscu docelowym.</span><span class="sxs-lookup"><span data-stu-id="6868c-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="6868c-111">To polecenie cmdlet nie zwraca zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="6868c-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="6868c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6868c-112">EXAMPLES</span></span>

### <span data-ttu-id="6868c-113">Przykład 1. Pobieranie pliku z folderu</span><span class="sxs-lookup"><span data-stu-id="6868c-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="6868c-114">To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z folderu udziału pliku ContosoShare06 do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="6868c-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="6868c-115">Przykład 2: pobranie plików w obszarze przykładowy udział plików</span><span class="sxs-lookup"><span data-stu-id="6868c-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="6868c-116">W tym przykładzie udostępniono pliki w obszarze przykładowego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="6868c-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="6868c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6868c-117">PARAMETERS</span></span>

### <span data-ttu-id="6868c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6868c-118">-AsJob</span></span>
<span data-ttu-id="6868c-119">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="6868c-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6868c-120">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="6868c-120">-CheckMd5</span></span>
<span data-ttu-id="6868c-121">Określa, czy ma być sprawdzana suma Md5 dla pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="6868c-121">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="6868c-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6868c-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6868c-123">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="6868c-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="6868c-124">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="6868c-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="6868c-125">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="6868c-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6868c-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6868c-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6868c-127">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6868c-127">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="6868c-128">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="6868c-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="6868c-129">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="6868c-129">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="6868c-130">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="6868c-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="6868c-131">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="6868c-131">The default value is 10.</span></span>

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

### <span data-ttu-id="6868c-132">-Context</span><span class="sxs-lookup"><span data-stu-id="6868c-132">-Context</span></span>
<span data-ttu-id="6868c-133">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6868c-133">Specifies an Azure Storage context.</span></span> <span data-ttu-id="6868c-134">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6868c-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6868c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6868c-135">-DefaultProfile</span></span>
<span data-ttu-id="6868c-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6868c-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6868c-137">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="6868c-137">-Destination</span></span>
<span data-ttu-id="6868c-138">Określa ścieżkę docelową.</span><span class="sxs-lookup"><span data-stu-id="6868c-138">Specifies the destination path.</span></span>
<span data-ttu-id="6868c-139">To polecenie cmdlet pobiera zawartość pliku do lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6868c-139">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="6868c-140">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="6868c-140">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="6868c-141">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="6868c-141">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="6868c-142">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="6868c-142">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="6868c-143">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6868c-143">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="6868c-144">-Directory</span><span class="sxs-lookup"><span data-stu-id="6868c-144">-Directory</span></span>
<span data-ttu-id="6868c-145">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="6868c-145">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="6868c-146">To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6868c-146">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="6868c-147">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="6868c-147">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="6868c-148">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="6868c-148">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6868c-149">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="6868c-149">-File</span></span>
<span data-ttu-id="6868c-150">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="6868c-150">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="6868c-151">To polecenie cmdlet umożliwia pobieranie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6868c-151">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="6868c-152">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="6868c-152">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6868c-153">-Force</span><span class="sxs-lookup"><span data-stu-id="6868c-153">-Force</span></span>
<span data-ttu-id="6868c-154">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="6868c-154">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="6868c-155">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="6868c-155">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="6868c-156">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="6868c-156">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="6868c-157">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6868c-157">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="6868c-158">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6868c-158">-PassThru</span></span>
<span data-ttu-id="6868c-159">Wskazuje, że to polecenie cmdlet zwróci obiekt **AzureStorageFile** , który jest przez niego pobierany.</span><span class="sxs-lookup"><span data-stu-id="6868c-159">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="6868c-160">-Path</span><span class="sxs-lookup"><span data-stu-id="6868c-160">-Path</span></span>
<span data-ttu-id="6868c-161">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="6868c-161">Specifies the path of a file.</span></span>
<span data-ttu-id="6868c-162">Ten aplet polecenia pobiera zawartość pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6868c-162">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="6868c-163">Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="6868c-163">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6868c-164">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6868c-164">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6868c-165">Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="6868c-165">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="6868c-166">Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="6868c-166">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6868c-167">-Share</span><span class="sxs-lookup"><span data-stu-id="6868c-167">-Share</span></span>
<span data-ttu-id="6868c-168">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="6868c-168">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="6868c-169">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6868c-169">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="6868c-170">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="6868c-170">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="6868c-171">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6868c-171">This object contains the storage context.</span></span>
<span data-ttu-id="6868c-172">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="6868c-172">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6868c-173">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="6868c-173">-ShareName</span></span>
<span data-ttu-id="6868c-174">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="6868c-174">Specifies the name of the file share.</span></span>
<span data-ttu-id="6868c-175">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6868c-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="6868c-176">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6868c-176">-Confirm</span></span>
<span data-ttu-id="6868c-177">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6868c-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6868c-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6868c-178">-WhatIf</span></span>
<span data-ttu-id="6868c-179">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6868c-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6868c-180">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6868c-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6868c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6868c-181">CommonParameters</span></span>
<span data-ttu-id="6868c-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6868c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6868c-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6868c-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6868c-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6868c-184">INPUTS</span></span>

### <span data-ttu-id="6868c-185">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="6868c-185">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="6868c-186">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="6868c-186">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="6868c-187">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="6868c-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="6868c-188">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6868c-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6868c-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6868c-189">OUTPUTS</span></span>

### <span data-ttu-id="6868c-190">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="6868c-190">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="6868c-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6868c-191">NOTES</span></span>

## <span data-ttu-id="6868c-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6868c-192">RELATED LINKS</span></span>

[<span data-ttu-id="6868c-193">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="6868c-193">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="6868c-194">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6868c-194">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


