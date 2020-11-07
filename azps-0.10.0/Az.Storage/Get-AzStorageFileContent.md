---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892234"
---
# <span data-ttu-id="5914d-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5914d-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="5914d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5914d-102">SYNOPSIS</span></span>
<span data-ttu-id="5914d-103">Umożliwia pobranie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="5914d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5914d-104">SYNTAX</span></span>

### <span data-ttu-id="5914d-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5914d-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5914d-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="5914d-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5914d-107">Directory</span><span class="sxs-lookup"><span data-stu-id="5914d-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5914d-108">Plik</span><span class="sxs-lookup"><span data-stu-id="5914d-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5914d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5914d-109">DESCRIPTION</span></span>
<span data-ttu-id="5914d-110">Polecenie cmdlet **Get-AzStorageFileContent** pobiera zawartość pliku, a następnie zapisuje je w określonym miejscu docelowym.</span><span class="sxs-lookup"><span data-stu-id="5914d-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="5914d-111">To polecenie cmdlet nie zwraca zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="5914d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5914d-112">EXAMPLES</span></span>

### <span data-ttu-id="5914d-113">Przykład 1. Pobieranie pliku z folderu</span><span class="sxs-lookup"><span data-stu-id="5914d-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="5914d-114">To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z folderu udziału pliku ContosoShare06 do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="5914d-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="5914d-115">Przykład 2: pobranie plików w obszarze przykładowy udział plików</span><span class="sxs-lookup"><span data-stu-id="5914d-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="5914d-116">W tym przykładzie udostępniono pliki w obszarze przykładowego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="5914d-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="5914d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5914d-117">PARAMETERS</span></span>

### <span data-ttu-id="5914d-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="5914d-118">-CheckMd5</span></span>
<span data-ttu-id="5914d-119">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-120">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-121">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-122">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5914d-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5914d-124">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-125">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-126">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-127">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5914d-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5914d-129">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-130">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-131">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-132">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-133">-Context</span><span class="sxs-lookup"><span data-stu-id="5914d-133">-Context</span></span>
<span data-ttu-id="5914d-134">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-135">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-136">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-137">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5914d-138">-DefaultProfile</span></span>
<span data-ttu-id="5914d-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5914d-140">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="5914d-140">-Destination</span></span>
<span data-ttu-id="5914d-141">Określa ścieżkę docelową.</span><span class="sxs-lookup"><span data-stu-id="5914d-141">Specifies the destination path.</span></span>
<span data-ttu-id="5914d-142">To polecenie cmdlet pobiera zawartość pliku do lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="5914d-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="5914d-143">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-144">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-145">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-146">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-147">-Directory</span><span class="sxs-lookup"><span data-stu-id="5914d-147">-Directory</span></span>
<span data-ttu-id="5914d-148">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="5914d-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="5914d-149">To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5914d-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="5914d-150">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="5914d-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="5914d-151">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="5914d-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="5914d-152">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="5914d-152">-File</span></span>
<span data-ttu-id="5914d-153">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="5914d-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="5914d-154">To polecenie cmdlet umożliwia pobieranie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5914d-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="5914d-155">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="5914d-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="5914d-156">-Force</span><span class="sxs-lookup"><span data-stu-id="5914d-156">-Force</span></span>
<span data-ttu-id="5914d-157">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-158">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-159">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-160">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5914d-161">-PassThru</span></span>
<span data-ttu-id="5914d-162">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-163">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-164">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-165">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-166">-Path</span><span class="sxs-lookup"><span data-stu-id="5914d-166">-Path</span></span>
<span data-ttu-id="5914d-167">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-167">Specifies the path of a file.</span></span>
<span data-ttu-id="5914d-168">Ten aplet polecenia pobiera zawartość pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5914d-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="5914d-169">Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="5914d-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5914d-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5914d-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5914d-171">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="5914d-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="5914d-172">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="5914d-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="5914d-173">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="5914d-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="5914d-174">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5914d-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="5914d-175">-Share</span><span class="sxs-lookup"><span data-stu-id="5914d-175">-Share</span></span>
<span data-ttu-id="5914d-176">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="5914d-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="5914d-177">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="5914d-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="5914d-178">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="5914d-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="5914d-179">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="5914d-179">This object contains the storage context.</span></span>
<span data-ttu-id="5914d-180">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="5914d-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="5914d-181">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="5914d-181">-ShareName</span></span>
<span data-ttu-id="5914d-182">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="5914d-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="5914d-183">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="5914d-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="5914d-184">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5914d-184">-Confirm</span></span>
<span data-ttu-id="5914d-185">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5914d-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5914d-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5914d-186">-WhatIf</span></span>
<span data-ttu-id="5914d-187">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5914d-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5914d-188">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5914d-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5914d-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5914d-189">CommonParameters</span></span>
<span data-ttu-id="5914d-190">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5914d-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5914d-191">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5914d-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5914d-192">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5914d-192">INPUTS</span></span>

### <span data-ttu-id="5914d-193">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="5914d-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="5914d-194">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5914d-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="5914d-195">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="5914d-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="5914d-196">Parametry: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5914d-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="5914d-197">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="5914d-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="5914d-198">Parametry: plik (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5914d-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="5914d-199">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5914d-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5914d-200">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5914d-200">OUTPUTS</span></span>

### <span data-ttu-id="5914d-201">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="5914d-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="5914d-202">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5914d-202">NOTES</span></span>

## <span data-ttu-id="5914d-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5914d-203">RELATED LINKS</span></span>

[<span data-ttu-id="5914d-204">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="5914d-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="5914d-205">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5914d-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


