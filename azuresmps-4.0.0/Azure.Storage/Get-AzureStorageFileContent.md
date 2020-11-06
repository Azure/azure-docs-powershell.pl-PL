---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
ms.openlocfilehash: c945838d7d237fb37610d3763525b0ecac838fbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524029"
---
# <span data-ttu-id="9ae5f-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9ae5f-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="9ae5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ae5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae5f-103">Umożliwia pobranie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="9ae5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ae5f-104">SYNTAX</span></span>

### <span data-ttu-id="9ae5f-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9ae5f-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae5f-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="9ae5f-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae5f-107">Directory</span><span class="sxs-lookup"><span data-stu-id="9ae5f-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae5f-108">Plik</span><span class="sxs-lookup"><span data-stu-id="9ae5f-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ae5f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9ae5f-109">DESCRIPTION</span></span>
<span data-ttu-id="9ae5f-110">Polecenie cmdlet **Get-AzureStorageFileContent** pobiera zawartość pliku, a następnie zapisuje je w określonym miejscu docelowym.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="9ae5f-111">To polecenie cmdlet nie zwraca zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="9ae5f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ae5f-112">EXAMPLES</span></span>

### <span data-ttu-id="9ae5f-113">Przykład 1. Pobieranie pliku z folderu</span><span class="sxs-lookup"><span data-stu-id="9ae5f-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="9ae5f-114">To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z folderu udziału pliku ContosoShare06 do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

## <span data-ttu-id="9ae5f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ae5f-115">PARAMETERS</span></span>

### <span data-ttu-id="9ae5f-116">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="9ae5f-116">-CheckMd5</span></span>
<span data-ttu-id="9ae5f-117">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-117">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-118">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-118">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-119">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-119">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-120">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-120">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ae5f-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9ae5f-122">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-122">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-123">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-123">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-124">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-124">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-125">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-125">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9ae5f-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9ae5f-127">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-127">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-128">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-128">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-129">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-129">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-130">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-130">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-131">-Context</span><span class="sxs-lookup"><span data-stu-id="9ae5f-131">-Context</span></span>
<span data-ttu-id="9ae5f-132">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-132">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-133">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-133">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-134">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-134">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-135">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-135">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-136">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="9ae5f-136">-Destination</span></span>
<span data-ttu-id="9ae5f-137">Określa ścieżkę docelową.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-137">Specifies the destination path.</span></span>
<span data-ttu-id="9ae5f-138">To polecenie cmdlet pobiera zawartość pliku do lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-138">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="9ae5f-139">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-139">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-140">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-140">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-141">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-141">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-142">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-142">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-143">-Directory</span><span class="sxs-lookup"><span data-stu-id="9ae5f-143">-Directory</span></span>
<span data-ttu-id="9ae5f-144">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="9ae5f-144">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9ae5f-145">To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-145">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="9ae5f-146">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-146">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="9ae5f-147">Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-147">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="9ae5f-148">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="9ae5f-148">-File</span></span>
<span data-ttu-id="9ae5f-149">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="9ae5f-149">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="9ae5f-150">To polecenie cmdlet umożliwia pobieranie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-150">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="9ae5f-151">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-151">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="9ae5f-152">-Force</span><span class="sxs-lookup"><span data-stu-id="9ae5f-152">-Force</span></span>
<span data-ttu-id="9ae5f-153">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-153">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-154">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-154">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-155">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-155">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-156">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-156">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-157">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ae5f-157">-PassThru</span></span>
<span data-ttu-id="9ae5f-158">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-158">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-159">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-159">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-160">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-160">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-161">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-161">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-162">-Path</span><span class="sxs-lookup"><span data-stu-id="9ae5f-162">-Path</span></span>
<span data-ttu-id="9ae5f-163">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-163">Specifies the path of a file.</span></span>
<span data-ttu-id="9ae5f-164">Ten aplet polecenia pobiera zawartość pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="9ae5f-165">Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9ae5f-166">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ae5f-166">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9ae5f-167">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-167">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="9ae5f-168">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-168">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="9ae5f-169">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-169">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="9ae5f-170">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-170">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="9ae5f-171">-Share</span><span class="sxs-lookup"><span data-stu-id="9ae5f-171">-Share</span></span>
<span data-ttu-id="9ae5f-172">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="9ae5f-172">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9ae5f-173">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-173">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="9ae5f-174">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-174">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="9ae5f-175">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-175">This object contains the storage context.</span></span>
<span data-ttu-id="9ae5f-176">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="9ae5f-176">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9ae5f-177">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="9ae5f-177">-ShareName</span></span>
<span data-ttu-id="9ae5f-178">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-178">Specifies the name of the file share.</span></span>
<span data-ttu-id="9ae5f-179">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-179">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="9ae5f-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ae5f-180">-Confirm</span></span>
<span data-ttu-id="9ae5f-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae5f-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae5f-182">-WhatIf</span></span>
<span data-ttu-id="9ae5f-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ae5f-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae5f-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae5f-185">CommonParameters</span></span>
<span data-ttu-id="9ae5f-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae5f-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae5f-187">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae5f-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae5f-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ae5f-188">INPUTS</span></span>

## <span data-ttu-id="9ae5f-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ae5f-189">OUTPUTS</span></span>

## <span data-ttu-id="9ae5f-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ae5f-190">NOTES</span></span>

## <span data-ttu-id="9ae5f-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ae5f-191">RELATED LINKS</span></span>

[<span data-ttu-id="9ae5f-192">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="9ae5f-192">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="9ae5f-193">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9ae5f-193">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


