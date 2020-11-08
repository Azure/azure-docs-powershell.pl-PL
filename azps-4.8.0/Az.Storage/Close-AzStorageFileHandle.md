---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064677"
---
# <span data-ttu-id="1a1cb-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1a1cb-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="1a1cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1cb-103">Zamyka uchwyty plików udziału plików, katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="1a1cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a1cb-104">SYNTAX</span></span>

### <span data-ttu-id="1a1cb-105">ShareNameCloseAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1a1cb-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a1cb-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="1a1cb-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a1cb-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="1a1cb-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a1cb-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="1a1cb-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a1cb-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="1a1cb-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a1cb-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="1a1cb-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a1cb-111">Opis</span><span class="sxs-lookup"><span data-stu-id="1a1cb-111">DESCRIPTION</span></span>
<span data-ttu-id="1a1cb-112">Polecenie cmdlet **Close-AzStorageFileHandle** powoduje zamknięcie dojść do plików udziału plików lub katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="1a1cb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a1cb-113">EXAMPLES</span></span>

### <span data-ttu-id="1a1cb-114">Przykład 1: wyświetla wszystkie udziały plików bieżącego konta magazynu i zamyka cyklicznie wszystkie uchwyty plików udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="1a1cb-115">To polecenie wyświetla listę wszystkich udziałów plików bieżącego konta magazynu i zamyka cyklicznie wszystkie uchwyty plików udziałów plików...</span><span class="sxs-lookup"><span data-stu-id="1a1cb-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="1a1cb-116">Przykład 2: cykliczne Zamykanie wszystkich dojść do plików w katalogu plików oraz wyświetlanie liczby dojść do zamkniętego pliku</span><span class="sxs-lookup"><span data-stu-id="1a1cb-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="1a1cb-117">To polecenie powoduje zamknięcie wszystkich dojść do plików w katalogu plików i wyświetlenie liczby zamkniętych dojść do pliku.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="1a1cb-118">Przykład 3: zamknięcie wszystkich dojść do plików, które zostały otwarte 1 dzień temu w katalogu plików</span><span class="sxs-lookup"><span data-stu-id="1a1cb-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="1a1cb-119">To polecenie wyświetla cyklicznie wszystkie uchwyty plików w katalogu plików, filtruje uchwyty, które zostały otwarte 1 dzień temu, a następnie zamyka je.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="1a1cb-120">Przykład 4: zamknięcie wszystkich dojść do plików w pliku</span><span class="sxs-lookup"><span data-stu-id="1a1cb-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="1a1cb-121">To polecenie powoduje zamknięcie wszystkich dojść do plików w pliku.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="1a1cb-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a1cb-122">PARAMETERS</span></span>

### <span data-ttu-id="1a1cb-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a1cb-123">-AsJob</span></span>
<span data-ttu-id="1a1cb-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1a1cb-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a1cb-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a1cb-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a1cb-126">Maksymalny czas wykonywania wszystkich żądań po stronie klienta (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="1a1cb-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="1a1cb-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="1a1cb-127">-CloseAll</span></span>
<span data-ttu-id="1a1cb-128">Wymuszaj zamknięcie wszystkich dojść do plików.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="1a1cb-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a1cb-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a1cb-130">Całkowita liczba współbieżnych zadań asynchronicznych.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="1a1cb-131">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-131">The default value is 10.</span></span>

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

### <span data-ttu-id="1a1cb-132">-Context</span><span class="sxs-lookup"><span data-stu-id="1a1cb-132">-Context</span></span>
<span data-ttu-id="1a1cb-133">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="1a1cb-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="1a1cb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1cb-134">-DefaultProfile</span></span>
<span data-ttu-id="1a1cb-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a1cb-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="1a1cb-136">-Directory</span></span>
<span data-ttu-id="1a1cb-137">Obiekt CloudFileDirectory wskazuje podstawowy folder, w którym znajdują się pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="1a1cb-138">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="1a1cb-138">-File</span></span>
<span data-ttu-id="1a1cb-139">Obiekt CloudFile wskazuje uchwyt pliku do zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-139">CloudFile object indicated the file to close handle.</span></span>

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

### <span data-ttu-id="1a1cb-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="1a1cb-140">-FileHandle</span></span>
<span data-ttu-id="1a1cb-141">Uchwyt pliku do zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="1a1cb-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a1cb-142">-PassThru</span></span>
<span data-ttu-id="1a1cb-143">Zwraca liczbę zamkniętych dojść do plików.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="1a1cb-144">-Path</span><span class="sxs-lookup"><span data-stu-id="1a1cb-144">-Path</span></span>
<span data-ttu-id="1a1cb-145">Ścieżka do istniejącego pliku/katalogu.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="1a1cb-146">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="1a1cb-146">-Recursive</span></span>
<span data-ttu-id="1a1cb-147">Lista dojść rekurencyjnych.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-147">List handles Recursively.</span></span>
<span data-ttu-id="1a1cb-148">Działa tylko w katalogu plików.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="1a1cb-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a1cb-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a1cb-150">Upłynął limit czasu serwera dla każdego żądania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="1a1cb-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="1a1cb-151">-Share</span><span class="sxs-lookup"><span data-stu-id="1a1cb-151">-Share</span></span>
<span data-ttu-id="1a1cb-152">Obiekt CloudFileShare wskazuje udział, w którym znajdują się listy plików/katalogów.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="1a1cb-153">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="1a1cb-153">-ShareName</span></span>
<span data-ttu-id="1a1cb-154">Nazwa udziału plików, w którym będą wyświetlane pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="1a1cb-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a1cb-155">-Confirm</span></span>
<span data-ttu-id="1a1cb-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a1cb-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a1cb-157">-WhatIf</span></span>
<span data-ttu-id="1a1cb-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a1cb-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a1cb-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1cb-160">CommonParameters</span></span>
<span data-ttu-id="1a1cb-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a1cb-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1cb-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a1cb-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1cb-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a1cb-163">INPUTS</span></span>

### <span data-ttu-id="1a1cb-164">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1a1cb-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="1a1cb-165">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="1a1cb-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="1a1cb-166">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a1cb-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a1cb-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a1cb-167">OUTPUTS</span></span>

### <span data-ttu-id="1a1cb-168">Microsoft. Azure. Storage. File. CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="1a1cb-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="1a1cb-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a1cb-169">NOTES</span></span>

## <span data-ttu-id="1a1cb-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a1cb-170">RELATED LINKS</span></span>
