---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224731"
---
# <span data-ttu-id="7114e-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7114e-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="7114e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7114e-102">SYNOPSIS</span></span>
<span data-ttu-id="7114e-103">Umożliwia przekazywanie zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="7114e-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="7114e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7114e-104">SYNTAX</span></span>

### <span data-ttu-id="7114e-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7114e-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7114e-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="7114e-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="7114e-107">Directory</span><span class="sxs-lookup"><span data-stu-id="7114e-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="7114e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7114e-108">DESCRIPTION</span></span>
<span data-ttu-id="7114e-109">Polecenie cmdlet **Set-AzStorageFileContent** umożliwia przekazywanie zawartości pliku do pliku w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="7114e-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="7114e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7114e-110">EXAMPLES</span></span>

### <span data-ttu-id="7114e-111">Przykład 1: przekazywanie pliku w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="7114e-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="7114e-112">To polecenie wysyła plik o nazwie DataFile37 w bieżącym folderze jako plik o nazwie CurrentDataFile w folderze o nazwie ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="7114e-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="7114e-113">Przykład 2: przekazywanie wszystkich plików w bieżącym folderze</span><span class="sxs-lookup"><span data-stu-id="7114e-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="7114e-114">W tym przykładzie użyto kilku typowych poleceń cmdlet programu Windows PowerShell i bieżącego polecenia cmdlet, aby przekazać wszystkie pliki z bieżącego folderu do folderu głównego kontenera ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="7114e-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="7114e-115">Pierwsze polecenie uzyskuje nazwę bieżącego folderu i zapisuje je w zmiennej $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="7114e-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="7114e-116">Drugie polecenie używa polecenia cmdlet **Get-AzStorageShare** w celu uzyskania udziału plików o nazwie ContosoShare06, a następnie zapisanie go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="7114e-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7114e-117">Polecenie ostatnie pobiera zawartość bieżącego folderu i przekazuje każdemu z nich do polecenia cmdlet Where-Object przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7114e-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7114e-118">Polecenie cmdlet umożliwia filtrowanie obiektów, które nie są plikami, a następnie przekazanie plików do polecenia cmdlet ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="7114e-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="7114e-119">Polecenie cmdlet uruchamia blok skryptu dla każdego pliku, który tworzy odpowiednią ścieżkę, a następnie używa bieżącego polecenia cmdlet do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="7114e-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="7114e-120">Wynik ma taką samą nazwę i taką samą położenie względne, co pozostałe pliki, które przykłada są ładowane.</span><span class="sxs-lookup"><span data-stu-id="7114e-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="7114e-121">Aby uzyskać więcej informacji na temat bloków skryptów, wpisz ciąg `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="7114e-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="7114e-122">Przykład 3: przekazywanie pliku lokalnego do pliku platformy Azure i perserve właściwości lokalnego pliku SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7114e-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="7114e-123">W tym przykładzie jest wysyłany plik lokalny do pliku systemu Azure, a perserves właściwości lokalnego pliku SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7114e-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="7114e-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7114e-124">PARAMETERS</span></span>

### <span data-ttu-id="7114e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7114e-125">-AsJob</span></span>
<span data-ttu-id="7114e-126">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="7114e-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7114e-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7114e-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7114e-128">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="7114e-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7114e-129">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="7114e-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7114e-130">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7114e-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7114e-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7114e-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7114e-132">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7114e-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7114e-133">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7114e-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7114e-134">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="7114e-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7114e-135">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="7114e-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7114e-136">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="7114e-136">The default value is 10.</span></span>

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

### <span data-ttu-id="7114e-137">-Context</span><span class="sxs-lookup"><span data-stu-id="7114e-137">-Context</span></span>
<span data-ttu-id="7114e-138">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7114e-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7114e-139">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="7114e-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7114e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7114e-140">-DefaultProfile</span></span>
<span data-ttu-id="7114e-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7114e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7114e-142">-Directory</span><span class="sxs-lookup"><span data-stu-id="7114e-142">-Directory</span></span>
<span data-ttu-id="7114e-143">Określa folder jako obiekt **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="7114e-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7114e-144">To polecenie cmdlet umożliwia przekazanie pliku do folderu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7114e-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="7114e-145">Aby uzyskać katalog, użyj polecenia cmdlet New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="7114e-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7114e-146">Możesz również użyć polecenia cmdlet Get-AzStorageFile, aby uzyskać katalog.</span><span class="sxs-lookup"><span data-stu-id="7114e-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="7114e-147">-Force</span><span class="sxs-lookup"><span data-stu-id="7114e-147">-Force</span></span>
<span data-ttu-id="7114e-148">Wskazuje, że to polecenie cmdlet zastępuje istniejący plik magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7114e-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="7114e-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7114e-149">-PassThru</span></span>
<span data-ttu-id="7114e-150">Wskazuje, że to polecenie cmdlet zwraca obiekt **AzureStorageFile** , który tworzy lub przekazuje.</span><span class="sxs-lookup"><span data-stu-id="7114e-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="7114e-151">-Path</span><span class="sxs-lookup"><span data-stu-id="7114e-151">-Path</span></span>
<span data-ttu-id="7114e-152">Określa ścieżkę do pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="7114e-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="7114e-153">To polecenie cmdlet umożliwia przekazywanie zawartości do pliku, który jest określany przez ten parametr, lub do pliku w folderze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7114e-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="7114e-154">Jeśli określisz folder, to polecenie cmdlet utworzy plik mający taką samą nazwę jak plik źródłowy.</span><span class="sxs-lookup"><span data-stu-id="7114e-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="7114e-155">Jeśli określisz ścieżkę pliku, który nie istnieje, to polecenie cmdlet spowoduje utworzenie tego pliku i zapisanie jego zawartości w tym pliku.</span><span class="sxs-lookup"><span data-stu-id="7114e-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="7114e-156">Jeśli określisz plik, który już istnieje, i określisz parametr _Force_ , to polecenie cmdlet zastąpi zawartość pliku.</span><span class="sxs-lookup"><span data-stu-id="7114e-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="7114e-157">Jeśli określisz plik, który już istnieje, i nie określisz _siły_ , to polecenie cmdlet nie zmieni się i zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7114e-157">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="7114e-158">Jeśli określisz ścieżkę do folderu, który nie istnieje, to polecenie cmdlet nie zmieni się i zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7114e-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="7114e-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="7114e-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="7114e-160">Zachowanie właściwości pliku źródłowego SMB (plik attributtes, czas tworzenia pliku, czas ostatniego zapisu pliku) w pliku docelowym.</span><span class="sxs-lookup"><span data-stu-id="7114e-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="7114e-161">Ten parametr jest dostępny tylko w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="7114e-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="7114e-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7114e-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7114e-163">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="7114e-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7114e-164">-Share</span><span class="sxs-lookup"><span data-stu-id="7114e-164">-Share</span></span>
<span data-ttu-id="7114e-165">Określa obiekt **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="7114e-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7114e-166">To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7114e-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="7114e-167">Aby uzyskać obiekt **CloudFileShare** , użyj polecenia cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="7114e-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="7114e-168">Ten obiekt zawiera kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="7114e-168">This object contains the storage context.</span></span>
<span data-ttu-id="7114e-169">W przypadku określenia tego parametru nie określaj parametru *kontekstu* .</span><span class="sxs-lookup"><span data-stu-id="7114e-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="7114e-170">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="7114e-170">-ShareName</span></span>
<span data-ttu-id="7114e-171">Określa nazwę udziału plików.</span><span class="sxs-lookup"><span data-stu-id="7114e-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="7114e-172">To polecenie cmdlet przekazuje do pliku w udziale pliku ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7114e-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="7114e-173">-Source</span><span class="sxs-lookup"><span data-stu-id="7114e-173">-Source</span></span>
<span data-ttu-id="7114e-174">Określa plik źródłowy, który jest wysyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7114e-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="7114e-175">Jeśli określisz plik, który nie istnieje, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="7114e-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7114e-176">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7114e-176">-Confirm</span></span>
<span data-ttu-id="7114e-177">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7114e-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7114e-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7114e-178">-WhatIf</span></span>
<span data-ttu-id="7114e-179">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7114e-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7114e-180">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7114e-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7114e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7114e-181">CommonParameters</span></span>
<span data-ttu-id="7114e-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7114e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7114e-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7114e-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7114e-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7114e-184">INPUTS</span></span>

### <span data-ttu-id="7114e-185">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7114e-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="7114e-186">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7114e-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="7114e-187">System. String</span><span class="sxs-lookup"><span data-stu-id="7114e-187">System.String</span></span>

### <span data-ttu-id="7114e-188">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7114e-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7114e-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7114e-189">OUTPUTS</span></span>

### <span data-ttu-id="7114e-190">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="7114e-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="7114e-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7114e-191">NOTES</span></span>

## <span data-ttu-id="7114e-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7114e-192">RELATED LINKS</span></span>

[<span data-ttu-id="7114e-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7114e-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="7114e-194">Nowe — AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7114e-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="7114e-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7114e-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
