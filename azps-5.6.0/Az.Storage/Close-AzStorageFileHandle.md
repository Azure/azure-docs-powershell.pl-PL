---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 71985cc978425c343e535e6455172f61e5397934
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988765"
---
# <span data-ttu-id="14b42-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="14b42-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="14b42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b42-102">SYNOPSIS</span></span>
<span data-ttu-id="14b42-103">Zamyka uchwyty udziału plików, katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="14b42-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="14b42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14b42-104">SYNTAX</span></span>

### <span data-ttu-id="14b42-105">ShareNameCloseAll (domyślne)</span><span class="sxs-lookup"><span data-stu-id="14b42-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b42-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="14b42-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14b42-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="14b42-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14b42-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="14b42-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14b42-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="14b42-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14b42-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="14b42-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14b42-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="14b42-111">DESCRIPTION</span></span>
<span data-ttu-id="14b42-112">Polecenie cmdlet **Close-AzStorageFileHandle** zamyka uchwyty pliku udziału plików, katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="14b42-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="14b42-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14b42-113">EXAMPLES</span></span>

### <span data-ttu-id="14b42-114">Przykład 1. Wyświetla listę wszystkich udziałów plików bieżącego konta magazynu i rekurencyjnie zamyka wszystkie uchwyty plików udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="14b42-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="14b42-115">To polecenie wyświetla listę wszystkich udziałów plików bieżącego konta magazynu i rekurencyjnie zamyka wszystkie uchwyty plików udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="14b42-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="14b42-116">Przykład 2. Ponowne zamykanie wszystkich uchwytów plików w katalogu plików i wyświetlanie liczby uchwytów zamkniętego pliku</span><span class="sxs-lookup"><span data-stu-id="14b42-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="14b42-117">To polecenie zamyka wszystkie uchwyty plików w katalogu plików i wyświetla liczbę zamkniętych uchwytów plików.</span><span class="sxs-lookup"><span data-stu-id="14b42-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="14b42-118">Przykład 3. Zamknięcie wszystkich uchwytów plików otwieranych 1 dzień temu w katalogu plików</span><span class="sxs-lookup"><span data-stu-id="14b42-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="14b42-119">To polecenie wyświetla listę wszystkich uchwytów pliku w katalogu plików, odfiltrowuje uchwyty otwarte 1 dzień temu, a następnie je zamyka.</span><span class="sxs-lookup"><span data-stu-id="14b42-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="14b42-120">Przykład 4. Zamknięcie wszystkich uchwytów pliku</span><span class="sxs-lookup"><span data-stu-id="14b42-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="14b42-121">To polecenie zamyka wszystkie uchwyty pliku.</span><span class="sxs-lookup"><span data-stu-id="14b42-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="14b42-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14b42-122">PARAMETERS</span></span>

### <span data-ttu-id="14b42-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="14b42-123">-AsJob</span></span>
<span data-ttu-id="14b42-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="14b42-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14b42-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14b42-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="14b42-126">Maksymalny czas wykonywania po stronie klienta dla każdego żądania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="14b42-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="14b42-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="14b42-127">-CloseAll</span></span>
<span data-ttu-id="14b42-128">Wymusz zamknięcie wszystkich uchwytów pliku.</span><span class="sxs-lookup"><span data-stu-id="14b42-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="14b42-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="14b42-130">Całkowita ilość jednoczesnych zadań synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="14b42-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="14b42-131">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="14b42-131">The default value is 10.</span></span>

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

### <span data-ttu-id="14b42-132">— kontekst</span><span class="sxs-lookup"><span data-stu-id="14b42-132">-Context</span></span>
<span data-ttu-id="14b42-133">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="14b42-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b42-134">-DefaultProfile</span></span>
<span data-ttu-id="14b42-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14b42-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b42-136">— Katalog</span><span class="sxs-lookup"><span data-stu-id="14b42-136">-Directory</span></span>
<span data-ttu-id="14b42-137">Obiekt CloudFileDirectory wskazywał folder bazowy, w którym będą wymienione pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="14b42-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-138">— Plik</span><span class="sxs-lookup"><span data-stu-id="14b42-138">-File</span></span>
<span data-ttu-id="14b42-139">Obiekt CloudFile wskazywał plik do zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="14b42-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="14b42-140">-FileHandle</span></span>
<span data-ttu-id="14b42-141">Uchwyt pliku do zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="14b42-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14b42-142">-PassThru</span></span>
<span data-ttu-id="14b42-143">Zwraca liczbę uchwytów zamkniętego pliku.</span><span class="sxs-lookup"><span data-stu-id="14b42-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="14b42-144">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="14b42-144">-Path</span></span>
<span data-ttu-id="14b42-145">Ścieżka do istniejącego pliku/katalogu.</span><span class="sxs-lookup"><span data-stu-id="14b42-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-146">- Rekurencyjna</span><span class="sxs-lookup"><span data-stu-id="14b42-146">-Recursive</span></span>
<span data-ttu-id="14b42-147">Uchwyty listy rekurencyjnie.</span><span class="sxs-lookup"><span data-stu-id="14b42-147">List handles Recursively.</span></span>
<span data-ttu-id="14b42-148">Działa tylko w katalogu plików.</span><span class="sxs-lookup"><span data-stu-id="14b42-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14b42-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="14b42-150">Czas serwera dla każdego żądania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="14b42-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="14b42-151">— Udostępnij</span><span class="sxs-lookup"><span data-stu-id="14b42-151">-Share</span></span>
<span data-ttu-id="14b42-152">Obiekt CloudFileShare wskazywał udział, w którym będą wyświetlane pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="14b42-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="14b42-153">-ShareName</span></span>
<span data-ttu-id="14b42-154">Nazwa udziału plików, w którym będą wyświetlane pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="14b42-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-155">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14b42-155">-Confirm</span></span>
<span data-ttu-id="14b42-156">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="14b42-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b42-157">-WhatIf</span></span>
<span data-ttu-id="14b42-158">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14b42-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14b42-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="14b42-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b42-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b42-160">CommonParameters</span></span>
<span data-ttu-id="14b42-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b42-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b42-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b42-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b42-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14b42-163">INPUTS</span></span>

### <span data-ttu-id="14b42-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="14b42-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="14b42-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="14b42-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="14b42-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14b42-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="14b42-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14b42-167">OUTPUTS</span></span>

### <span data-ttu-id="14b42-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="14b42-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="14b42-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14b42-169">NOTES</span></span>

## <span data-ttu-id="14b42-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14b42-170">RELATED LINKS</span></span>
