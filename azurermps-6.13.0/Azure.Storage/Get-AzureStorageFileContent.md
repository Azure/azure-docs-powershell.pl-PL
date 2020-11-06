---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 0641fdf635bce2bbb545e50ecc99a39329fabc9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544020"
---
# <span data-ttu-id="e2a52-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e2a52-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="e2a52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2a52-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a52-103">Umożliwia pobranie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2a52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2a52-104">SYNTAX</span></span>

### <span data-ttu-id="e2a52-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e2a52-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a52-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="e2a52-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a52-107">Directory</span><span class="sxs-lookup"><span data-stu-id="e2a52-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a52-108">Plik</span><span class="sxs-lookup"><span data-stu-id="e2a52-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2a52-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e2a52-109">DESCRIPTION</span></span>
<span data-ttu-id="e2a52-110">Polecenie cmdlet **Get-AzureStorageFileContent** pobiera zawartość pliku, a następnie zapisuje je w określonym miejscu docelowym.</span><span class="sxs-lookup"><span data-stu-id="e2a52-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="e2a52-111">To polecenie cmdlet nie zwraca zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="e2a52-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2a52-112">EXAMPLES</span></span>

### <span data-ttu-id="e2a52-113">Przykład 1. Pobieranie pliku z folderu</span><span class="sxs-lookup"><span data-stu-id="e2a52-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="e2a52-114">To polecenie pobiera plik o nazwie CurrentDataFile w folderze ContosoWorkingFolder z folderu udziału pliku ContosoShare06 do bieżącego folderu.</span><span class="sxs-lookup"><span data-stu-id="e2a52-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="e2a52-115">Przykład 2: pobranie plików w obszarze przykładowy udział plików</span><span class="sxs-lookup"><span data-stu-id="e2a52-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="e2a52-116">W tym przykładzie udostępniono pliki w obszarze przykładowego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e2a52-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="e2a52-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2a52-117">PARAMETERS</span></span>

### <span data-ttu-id="e2a52-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="e2a52-118">-CheckMd5</span></span>
<span data-ttu-id="e2a52-119">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-120">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-121">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-122">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2a52-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e2a52-124">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-125">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-126">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-127">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e2a52-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e2a52-129">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-130">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-131">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-132">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-133">-Context</span><span class="sxs-lookup"><span data-stu-id="e2a52-133">-Context</span></span>
<span data-ttu-id="e2a52-134">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-135">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-136">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-137">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a52-138">-DefaultProfile</span></span>
<span data-ttu-id="e2a52-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a52-140">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="e2a52-140">-Destination</span></span>
<span data-ttu-id="e2a52-141">Określa ścieżkę docelową.</span><span class="sxs-lookup"><span data-stu-id="e2a52-141">Specifies the destination path.</span></span>
<span data-ttu-id="e2a52-142">To polecenie cmdlet pobiera zawartość pliku do lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="e2a52-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="e2a52-143">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-144">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-145">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-146">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-147">-Directory</span><span class="sxs-lookup"><span data-stu-id="e2a52-147">-Directory</span></span>
<span data-ttu-id="e2a52-148">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="e2a52-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="e2a52-149">To polecenie cmdlet pobiera zawartość pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e2a52-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="e2a52-150">Aby uzyskać katalog, użyj polecenia cmdlet New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="e2a52-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="e2a52-151">Możesz również użyć polecenia cmdlet Get-AzureStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="e2a52-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="e2a52-152">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="e2a52-152">-File</span></span>
<span data-ttu-id="e2a52-153">Określa plik jako obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="e2a52-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="e2a52-154">To polecenie cmdlet umożliwia pobieranie pliku, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e2a52-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="e2a52-155">Aby uzyskać obiekt **CloudFile** , użyj polecenia cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="e2a52-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="e2a52-156">-Force</span><span class="sxs-lookup"><span data-stu-id="e2a52-156">-Force</span></span>
<span data-ttu-id="e2a52-157">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-158">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-159">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-160">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2a52-161">-PassThru</span></span>
<span data-ttu-id="e2a52-162">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-163">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-164">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-165">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-166">-Path</span><span class="sxs-lookup"><span data-stu-id="e2a52-166">-Path</span></span>
<span data-ttu-id="e2a52-167">Określa ścieżkę pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-167">Specifies the path of a file.</span></span>
<span data-ttu-id="e2a52-168">Ten aplet polecenia pobiera zawartość pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e2a52-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="e2a52-169">Jeśli plik nie istnieje, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="e2a52-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e2a52-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2a52-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e2a52-171">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie zawartości w nowym pliku.</span><span class="sxs-lookup"><span data-stu-id="e2a52-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e2a52-172">Jeśli określisz ścieżkę do pliku, który już istnieje, i określisz parametr *Force* , polecenie cmdlet zastępuje plik.</span><span class="sxs-lookup"><span data-stu-id="e2a52-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e2a52-173">Jeśli określisz ścieżkę do istniejącego pliku i nie określisz *siły* , polecenie cmdlet wyświetli monit przed kontynuacją.</span><span class="sxs-lookup"><span data-stu-id="e2a52-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e2a52-174">Jeśli określisz ścieżkę folderu, to polecenie cmdlet podejmie próbę utworzenia pliku zawierającego nazwę pliku magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a52-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e2a52-175">-Share</span><span class="sxs-lookup"><span data-stu-id="e2a52-175">-Share</span></span>
<span data-ttu-id="e2a52-176">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="e2a52-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e2a52-177">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="e2a52-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="e2a52-178">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e2a52-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="e2a52-179">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e2a52-179">This object contains the storage context.</span></span>
<span data-ttu-id="e2a52-180">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="e2a52-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="e2a52-181">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="e2a52-181">-ShareName</span></span>
<span data-ttu-id="e2a52-182">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e2a52-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="e2a52-183">To polecenie cmdlet pobiera zawartość pliku w polu Udostępnij ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="e2a52-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="e2a52-184">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2a52-184">-Confirm</span></span>
<span data-ttu-id="e2a52-185">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2a52-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a52-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a52-186">-WhatIf</span></span>
<span data-ttu-id="e2a52-187">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2a52-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2a52-188">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2a52-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a52-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a52-189">CommonParameters</span></span>
<span data-ttu-id="e2a52-190">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a52-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a52-191">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a52-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a52-192">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2a52-192">INPUTS</span></span>

### <span data-ttu-id="e2a52-193">Microsoft. platformy windowsazure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e2a52-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="e2a52-194">Parametry: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2a52-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="e2a52-195">Microsoft. platformy windowsazure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="e2a52-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="e2a52-196">Parametry: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2a52-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="e2a52-197">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e2a52-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="e2a52-198">Parametry: plik (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2a52-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="e2a52-199">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2a52-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e2a52-200">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2a52-200">OUTPUTS</span></span>

### <span data-ttu-id="e2a52-201">Microsoft. platformy windowsazure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e2a52-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="e2a52-202">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2a52-202">NOTES</span></span>

## <span data-ttu-id="e2a52-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2a52-203">RELATED LINKS</span></span>

[<span data-ttu-id="e2a52-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e2a52-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="e2a52-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e2a52-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


