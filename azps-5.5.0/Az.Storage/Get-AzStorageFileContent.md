---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176658"
---
# <span data-ttu-id="7f4e4-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7f4e4-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="7f4e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f4e4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4e4-103">Pobiera zawartość pliku.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="7f4e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7f4e4-104">SYNTAX</span></span>

### <span data-ttu-id="7f4e4-105">ShareName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="7f4e4-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7f4e4-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="7f4e4-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7f4e4-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="7f4e4-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7f4e4-108">Plik</span><span class="sxs-lookup"><span data-stu-id="7f4e4-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="7f4e4-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7f4e4-109">DESCRIPTION</span></span>
<span data-ttu-id="7f4e4-110">Polecenie **cmdlet Get-AzStorageFileContent** pobiera zawartość pliku, a następnie zapisuje go w określone przez Ciebie lokalizacji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="7f4e4-111">To polecenie cmdlet nie zwraca zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="7f4e4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7f4e4-112">EXAMPLES</span></span>

### <span data-ttu-id="7f4e4-113">Przykład 1. Pobieranie pliku z folderu</span><span class="sxs-lookup"><span data-stu-id="7f4e4-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="7f4e4-114">To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z udziału plików ContosoShare06 do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="7f4e4-115">Przykład 2. Pobieranie plików z przykładowego udziału plików</span><span class="sxs-lookup"><span data-stu-id="7f4e4-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="7f4e4-116">W tym przykładzie są pobierane pliki z przykładowego udziału plików</span><span class="sxs-lookup"><span data-stu-id="7f4e4-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="7f4e4-117">Przykład 3. Pobieranie pliku platformy Azure do pliku lokalnego i korzystanie z właściwości SMB pliku platformy Azure (Attributtes file Attributtes, File Creation Time, File Last Write Time) w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="7f4e4-118">W tym przykładzie plik platformy Azure jest pobierany do pliku lokalnego i ma właściwości SMB pliku platformy Azure (Attributtes, File Creation Time, File Last Write Time) w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="7f4e4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f4e4-119">PARAMETERS</span></span>

### <span data-ttu-id="7f4e4-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7f4e4-120">-AsJob</span></span>
<span data-ttu-id="7f4e4-121">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7f4e4-122">— CheckMd5</span><span class="sxs-lookup"><span data-stu-id="7f4e4-122">-CheckMd5</span></span>
<span data-ttu-id="7f4e4-123">Określa, czy należy sprawdzić sumę Md5 dla pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="7f4e4-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7f4e4-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7f4e4-125">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="7f4e4-126">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="7f4e4-127">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7f4e4-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7f4e4-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7f4e4-129">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="7f4e4-130">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="7f4e4-131">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="7f4e4-132">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="7f4e4-133">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-133">The default value is 10.</span></span>

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

### <span data-ttu-id="7f4e4-134">— kontekst</span><span class="sxs-lookup"><span data-stu-id="7f4e4-134">-Context</span></span>
<span data-ttu-id="7f4e4-135">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="7f4e4-136">Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7f4e4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4e4-137">-DefaultProfile</span></span>
<span data-ttu-id="7f4e4-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f4e4-139">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="7f4e4-139">-Destination</span></span>
<span data-ttu-id="7f4e4-140">Określa ścieżkę docelową.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-140">Specifies the destination path.</span></span>
<span data-ttu-id="7f4e4-141">To polecenie cmdlet pobiera zawartość pliku do lokalizacji, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="7f4e4-142">Jeśli określisz ścieżkę nieistniecego pliku, to polecenie cmdlet utworzy ten plik i zapisze zawartość nowego pliku.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7f4e4-143">Jeśli określisz ścieżkę pliku, który już istnieje, i określisz parametr *Force,* polecenie cmdlet zastąpi plik.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7f4e4-144">Jeśli określisz ścieżkę istniejącego pliku i nie określisz wymuś, polecenie cmdlet wyświetli monit przed kontynuowaniem.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7f4e4-145">Jeśli określisz ścieżkę folderu, to polecenie cmdlet spróbuje utworzyć plik, który ma nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7f4e4-146">— Katalog</span><span class="sxs-lookup"><span data-stu-id="7f4e4-146">-Directory</span></span>
<span data-ttu-id="7f4e4-147">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7f4e4-148">To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="7f4e4-149">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7f4e4-150">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="7f4e4-151">— Plik</span><span class="sxs-lookup"><span data-stu-id="7f4e4-151">-File</span></span>
<span data-ttu-id="7f4e4-152">Określa plik jako obiekt **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="7f4e4-153">To polecenie cmdlet pobiera plik, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="7f4e4-154">Aby uzyskać obiekt **CloudFile,** użyj Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e4-155">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7f4e4-155">-Force</span></span>
<span data-ttu-id="7f4e4-156">Jeśli określisz ścieżkę nieistniecego pliku, to polecenie cmdlet utworzy ten plik i zapisze zawartość nowego pliku.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7f4e4-157">Jeśli określisz ścieżkę pliku, który już istnieje, i określisz parametr *Force,* polecenie cmdlet zastąpi plik.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7f4e4-158">Jeśli określisz ścieżkę istniejącego pliku i nie określisz wymuś, polecenie cmdlet wyświetli monit przed kontynuowaniem.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7f4e4-159">Jeśli określisz ścieżkę folderu, to polecenie cmdlet spróbuje utworzyć plik, który ma nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7f4e4-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f4e4-160">-PassThru</span></span>
<span data-ttu-id="7f4e4-161">Wskazuje, że to polecenie cmdlet zwraca pobrany obiekt **AzureStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="7f4e4-162">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="7f4e4-162">-Path</span></span>
<span data-ttu-id="7f4e4-163">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-163">Specifies the path of a file.</span></span>
<span data-ttu-id="7f4e4-164">To polecenie cmdlet pobiera zawartość pliku określaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="7f4e4-165">Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7f4e4-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="7f4e4-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="7f4e4-167">Zachowaj właściwości źródłowego pliku SMB (Attributtes file, File Creation Time, File Last Write Time) w pliku docelowym.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="7f4e4-168">Ten parametr jest dostępny tylko w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="7f4e4-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7f4e4-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7f4e4-170">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="7f4e4-171">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7f4e4-172">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="7f4e4-172">-Share</span></span>
<span data-ttu-id="7f4e4-173">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7f4e4-174">To polecenie cmdlet pobiera zawartość pliku z udziału, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="7f4e4-175">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="7f4e4-176">Ten obiekt zawiera kontekst przechowywania.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-176">This object contains the storage context.</span></span>
<span data-ttu-id="7f4e4-177">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="7f4e4-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="7f4e4-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7f4e4-178">-ShareName</span></span>
<span data-ttu-id="7f4e4-179">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="7f4e4-180">To polecenie cmdlet pobiera zawartość pliku z udziału, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="7f4e4-181">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f4e4-181">-Confirm</span></span>
<span data-ttu-id="7f4e4-182">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4e4-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f4e4-183">-WhatIf</span></span>
<span data-ttu-id="7f4e4-184">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4e4-185">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4e4-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4e4-186">CommonParameters</span></span>
<span data-ttu-id="7f4e4-187">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4e4-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f4e4-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4e4-189">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f4e4-189">INPUTS</span></span>

### <span data-ttu-id="7f4e4-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7f4e4-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="7f4e4-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7f4e4-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="7f4e4-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="7f4e4-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="7f4e4-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7f4e4-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7f4e4-194">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f4e4-194">OUTPUTS</span></span>

### <span data-ttu-id="7f4e4-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="7f4e4-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="7f4e4-196">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7f4e4-196">NOTES</span></span>

## <span data-ttu-id="7f4e4-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f4e4-197">RELATED LINKS</span></span>

[<span data-ttu-id="7f4e4-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="7f4e4-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="7f4e4-199">Set-azstorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7f4e4-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


