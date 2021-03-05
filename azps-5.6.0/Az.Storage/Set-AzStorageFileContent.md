---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 597728b1b327da28495574ca865a2e75a1a774a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974161"
---
# <span data-ttu-id="1f537-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1f537-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="1f537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f537-102">SYNOPSIS</span></span>
<span data-ttu-id="1f537-103">Przekazanie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="1f537-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="1f537-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f537-104">SYNTAX</span></span>

### <span data-ttu-id="1f537-105">ShareName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1f537-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="1f537-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="1f537-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="1f537-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="1f537-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="1f537-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f537-108">DESCRIPTION</span></span>
<span data-ttu-id="1f537-109">Polecenie **cmdlet Set-AzStorageFileContent** przekaże zawartość pliku do pliku w określonym udostępniniu.</span><span class="sxs-lookup"><span data-stu-id="1f537-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="1f537-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f537-110">EXAMPLES</span></span>

### <span data-ttu-id="1f537-111">Przykład 1. Przekazywanie pliku w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="1f537-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="1f537-112">To polecenie przekaże plik o nazwie DataFile37 w bieżącym folderze jako plik o nazwie CurrentDataFile w folderze o nazwie ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="1f537-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="1f537-113">Przykład 2. Przekazywanie wszystkich plików w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="1f537-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="1f537-114">W tym przykładzie użyto kilku typowych poleceń cmdlet programu Windows PowerShell i bieżącego polecenia cmdlet w celu przekazania wszystkich plików z bieżącego folderu do folderu głównego kontenera ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="1f537-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="1f537-115">Pierwsze polecenie otrzymuje nazwę bieżącego folderu i zapisuje je w $CurrentFolder zmienną.</span><span class="sxs-lookup"><span data-stu-id="1f537-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="1f537-116">Drugie polecenie używa polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie zapisuje go w zmiennej $Container pliku.</span><span class="sxs-lookup"><span data-stu-id="1f537-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="1f537-117">Ostatnie polecenie pobiera zawartość bieżącego folderu i przekazuje je do Where-Object cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1f537-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1f537-118">To polecenie cmdlet odfiltrowuje obiekty, które nie są plikami, a następnie przekazuje pliki do ForEach-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f537-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="1f537-119">To polecenie cmdlet uruchamia blok skryptu dla każdego pliku, który tworzy odpowiednią ścieżkę dla tego pliku, a następnie używa bieżącego polecenia cmdlet do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="1f537-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="1f537-120">Wynik ma taką samą nazwę i tę samą pozycję względną względem innych plików, które zostały przesłane w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="1f537-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="1f537-121">Aby uzyskać więcej informacji na temat bloków skryptów, wpisz `Get-Help about_Script_Blocks` tekst.</span><span class="sxs-lookup"><span data-stu-id="1f537-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="1f537-122">Przykład 3. Przekazywanie pliku lokalnego do pliku platformy Azure i korzystanie z lokalnych właściwości plików SMB (Przydzielenie plików, Czas utworzenia pliku, Godzina ostatniego zapisu pliku) w pliku platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f537-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="1f537-123">W tym przykładzie plik lokalny jest przesyłany do pliku platformy Azure i zawiera właściwości lokalnego pliku SMB (Attributtes file Attributtes, File Creation Time, File Last Write Time) w pliku platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f537-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="1f537-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f537-124">PARAMETERS</span></span>

### <span data-ttu-id="1f537-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1f537-125">-AsJob</span></span>
<span data-ttu-id="1f537-126">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="1f537-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1f537-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f537-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1f537-128">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="1f537-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1f537-129">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="1f537-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1f537-130">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="1f537-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1f537-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1f537-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1f537-132">Określa maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1f537-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1f537-133">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="1f537-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1f537-134">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="1f537-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1f537-135">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="1f537-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1f537-136">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="1f537-136">The default value is 10.</span></span>

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

### <span data-ttu-id="1f537-137">— kontekst</span><span class="sxs-lookup"><span data-stu-id="1f537-137">-Context</span></span>
<span data-ttu-id="1f537-138">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f537-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1f537-139">Aby uzyskać kontekst przechowywania, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="1f537-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1f537-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f537-140">-DefaultProfile</span></span>
<span data-ttu-id="1f537-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f537-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f537-142">— Katalog</span><span class="sxs-lookup"><span data-stu-id="1f537-142">-Directory</span></span>
<span data-ttu-id="1f537-143">Określa folder jako obiekt **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="1f537-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1f537-144">To polecenie cmdlet przekaże plik do folderu, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1f537-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="1f537-145">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f537-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="1f537-146">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="1f537-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="1f537-147">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1f537-147">-Force</span></span>
<span data-ttu-id="1f537-148">Wskazuje, że to polecenie cmdlet zastępuje istniejący plik magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f537-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="1f537-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f537-149">-PassThru</span></span>
<span data-ttu-id="1f537-150">Wskazuje, że to polecenie cmdlet zwraca obiekt **AzureStorageFile,** który tworzy lub przesyła.</span><span class="sxs-lookup"><span data-stu-id="1f537-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="1f537-151">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="1f537-151">-Path</span></span>
<span data-ttu-id="1f537-152">Określa ścieżkę pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="1f537-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="1f537-153">To polecenie cmdlet przekaże zawartość do pliku, który ten parametr określa, lub do pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1f537-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="1f537-154">Jeśli określisz folder, to polecenie cmdlet utworzy plik o takiej samej nazwie jak plik źródłowy.</span><span class="sxs-lookup"><span data-stu-id="1f537-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="1f537-155">Jeśli określisz ścieżkę nieistniecego pliku, to polecenie cmdlet utworzy ten plik i zapisze jego zawartość.</span><span class="sxs-lookup"><span data-stu-id="1f537-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="1f537-156">Jeśli określisz plik, który już istnieje, i określisz parametr _Force,_ to polecenie cmdlet zastąpi zawartość pliku.</span><span class="sxs-lookup"><span data-stu-id="1f537-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="1f537-157">Jeśli określisz plik, który już istnieje, a nie określisz wymuszania, to polecenie cmdlet nie wprowadza żadnych zmian i zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="1f537-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="1f537-158">Jeśli określisz ścieżkę nieistniecego folderu, to polecenie cmdlet nie wprowadza żadnych zmian i zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="1f537-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="1f537-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="1f537-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="1f537-160">Zachowaj właściwości źródłowego pliku SMB (Attributtes file, File Creation Time, File Last Write Time) w pliku docelowym.</span><span class="sxs-lookup"><span data-stu-id="1f537-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="1f537-161">Ten parametr jest dostępny tylko w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="1f537-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="1f537-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f537-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1f537-163">Określa długość okresu przeoencji dla części żądania na serwerze.</span><span class="sxs-lookup"><span data-stu-id="1f537-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1f537-164">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="1f537-164">-Share</span></span>
<span data-ttu-id="1f537-165">Określa obiekt **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="1f537-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1f537-166">To polecenie cmdlet jest przekazywania do pliku w udział plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1f537-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="1f537-167">Aby uzyskać obiekt **CloudFileShare,** użyj Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f537-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="1f537-168">Ten obiekt zawiera kontekst przechowywania.</span><span class="sxs-lookup"><span data-stu-id="1f537-168">This object contains the storage context.</span></span>
<span data-ttu-id="1f537-169">Jeśli określisz ten parametr, nie określaj *parametru kontekstowego.*</span><span class="sxs-lookup"><span data-stu-id="1f537-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="1f537-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1f537-170">-ShareName</span></span>
<span data-ttu-id="1f537-171">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="1f537-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="1f537-172">To polecenie cmdlet jest przekazywania do pliku w udział plików, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1f537-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="1f537-173">— Źródło</span><span class="sxs-lookup"><span data-stu-id="1f537-173">-Source</span></span>
<span data-ttu-id="1f537-174">Określa plik źródłowy, który zostanie przekazanie przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f537-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="1f537-175">Jeśli określisz plik, który nie istnieje, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="1f537-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f537-176">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f537-176">-Confirm</span></span>
<span data-ttu-id="1f537-177">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f537-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f537-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f537-178">-WhatIf</span></span>
<span data-ttu-id="1f537-179">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f537-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f537-180">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f537-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f537-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f537-181">CommonParameters</span></span>
<span data-ttu-id="1f537-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f537-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f537-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f537-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f537-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f537-184">INPUTS</span></span>

### <span data-ttu-id="1f537-185">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1f537-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="1f537-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="1f537-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="1f537-187">System.String</span><span class="sxs-lookup"><span data-stu-id="1f537-187">System.String</span></span>

### <span data-ttu-id="1f537-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f537-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1f537-189">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f537-189">OUTPUTS</span></span>

### <span data-ttu-id="1f537-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1f537-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="1f537-191">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f537-191">NOTES</span></span>

## <span data-ttu-id="1f537-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f537-192">RELATED LINKS</span></span>

[<span data-ttu-id="1f537-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="1f537-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="1f537-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="1f537-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="1f537-195">Get-AzstorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1f537-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
