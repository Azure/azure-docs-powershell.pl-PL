---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 1dc1e95e2ecf085faad664f624e7595acd9ab607
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545931"
---
# <span data-ttu-id="2534f-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2534f-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="2534f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2534f-102">SYNOPSIS</span></span>
<span data-ttu-id="2534f-103">Umożliwia pobranie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2534f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2534f-104">SYNTAX</span></span>

### <span data-ttu-id="2534f-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2534f-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2534f-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="2534f-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2534f-107">Directory</span><span class="sxs-lookup"><span data-stu-id="2534f-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2534f-108">Plik</span><span class="sxs-lookup"><span data-stu-id="2534f-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2534f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2534f-109">DESCRIPTION</span></span>
<span data-ttu-id="2534f-110">Polecenie cmdlet **Get-AzureStorageFileContent** pobiera zawartość pliku, a następnie zapisuje je w określonym miejscu docelowym.</span><span class="sxs-lookup"><span data-stu-id="2534f-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="2534f-111">To polecenie cmdlet nie zwraca zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="2534f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2534f-112">EXAMPLES</span></span>

### <span data-ttu-id="2534f-113">Przykład 1. Pobieranie pliku z folderu</span><span class="sxs-lookup"><span data-stu-id="2534f-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="2534f-114">To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z folderu udziału pliku ContosoShare06 do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="2534f-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="2534f-115">Przykład 2: pobranie plików w obszarze przykładowy udział plików</span><span class="sxs-lookup"><span data-stu-id="2534f-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="2534f-116">W tym przykładzie udostępniono pliki w obszarze przykładowego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2534f-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="2534f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2534f-117">PARAMETERS</span></span>

### <span data-ttu-id="2534f-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="2534f-118">-CheckMd5</span></span>
<span data-ttu-id="2534f-119">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-120">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-121">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-122">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2534f-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2534f-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2534f-124">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-125">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-126">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-127">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2534f-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2534f-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2534f-129">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-130">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-131">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-132">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2534f-133">-Context</span><span class="sxs-lookup"><span data-stu-id="2534f-133">-Context</span></span>
<span data-ttu-id="2534f-134">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-135">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-136">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-137">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2534f-138">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="2534f-138">-Destination</span></span>
<span data-ttu-id="2534f-139">Określa ścieżkę docelową.</span><span class="sxs-lookup"><span data-stu-id="2534f-139">Specifies the destination path.</span></span>
<span data-ttu-id="2534f-140">To polecenie cmdlet pobiera zawartość pliku do lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2534f-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="2534f-141">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-142">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-143">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-144">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-145">-Directory</span><span class="sxs-lookup"><span data-stu-id="2534f-145">-Directory</span></span>
<span data-ttu-id="2534f-146">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="2534f-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2534f-147">To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2534f-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="2534f-148">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="2534f-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2534f-149">Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="2534f-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="2534f-150">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="2534f-150">-File</span></span>
<span data-ttu-id="2534f-151">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="2534f-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="2534f-152">To polecenie cmdlet umożliwia pobieranie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2534f-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="2534f-153">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="2534f-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="2534f-154">-Force</span><span class="sxs-lookup"><span data-stu-id="2534f-154">-Force</span></span>
<span data-ttu-id="2534f-155">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-156">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-157">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-158">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2534f-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2534f-159">-PassThru</span></span>
<span data-ttu-id="2534f-160">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-161">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-162">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-163">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2534f-164">-Path</span><span class="sxs-lookup"><span data-stu-id="2534f-164">-Path</span></span>
<span data-ttu-id="2534f-165">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-165">Specifies the path of a file.</span></span>
<span data-ttu-id="2534f-166">Ten aplet polecenia pobiera zawartość pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2534f-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="2534f-167">Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="2534f-167">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2534f-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2534f-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2534f-169">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="2534f-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2534f-170">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="2534f-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2534f-171">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="2534f-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2534f-172">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2534f-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2534f-173">-Share</span><span class="sxs-lookup"><span data-stu-id="2534f-173">-Share</span></span>
<span data-ttu-id="2534f-174">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="2534f-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2534f-175">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2534f-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="2534f-176">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="2534f-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="2534f-177">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="2534f-177">This object contains the storage context.</span></span>
<span data-ttu-id="2534f-178">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="2534f-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="2534f-179">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="2534f-179">-ShareName</span></span>
<span data-ttu-id="2534f-180">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="2534f-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="2534f-181">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2534f-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="2534f-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2534f-182">-Confirm</span></span>
<span data-ttu-id="2534f-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2534f-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2534f-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2534f-184">-WhatIf</span></span>
<span data-ttu-id="2534f-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2534f-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2534f-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2534f-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2534f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2534f-187">CommonParameters</span></span>
<span data-ttu-id="2534f-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2534f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2534f-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2534f-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2534f-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2534f-190">INPUTS</span></span>

### <span data-ttu-id="2534f-191">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2534f-191">IStorageContext</span></span>

<span data-ttu-id="2534f-192">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="2534f-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="2534f-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2534f-193">CloudFileDirectory</span></span>

<span data-ttu-id="2534f-194">Parametr "katalog" akceptuje wartość typu "CloudFileDirectory" z procesu</span><span class="sxs-lookup"><span data-stu-id="2534f-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="2534f-195">CloudFile</span><span class="sxs-lookup"><span data-stu-id="2534f-195">CloudFile</span></span>

<span data-ttu-id="2534f-196">Parametr "File" przyjmuje wartość typu "CloudFile" z procesu</span><span class="sxs-lookup"><span data-stu-id="2534f-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="2534f-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2534f-197">CloudFileShare</span></span>

<span data-ttu-id="2534f-198">Parametr "Udostępnij" akceptuje wartość typu "CloudFileShare" z procesu</span><span class="sxs-lookup"><span data-stu-id="2534f-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="2534f-199">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2534f-199">OUTPUTS</span></span>

## <span data-ttu-id="2534f-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2534f-200">NOTES</span></span>

## <span data-ttu-id="2534f-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2534f-201">RELATED LINKS</span></span>

[<span data-ttu-id="2534f-202">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="2534f-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="2534f-203">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2534f-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


