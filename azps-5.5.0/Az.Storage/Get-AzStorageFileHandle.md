---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187811"
---
# <span data-ttu-id="9e3d8-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="9e3d8-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="9e3d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3d8-103">Lista uchwytów pliku udziału plików, katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="9e3d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e3d8-104">SYNTAX</span></span>

### <span data-ttu-id="9e3d8-105">ShareName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9e3d8-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e3d8-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="9e3d8-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e3d8-107">Katalog</span><span class="sxs-lookup"><span data-stu-id="9e3d8-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e3d8-108">Plik</span><span class="sxs-lookup"><span data-stu-id="9e3d8-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="9e3d8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e3d8-109">DESCRIPTION</span></span>
<span data-ttu-id="9e3d8-110">Polecenie **cmdlet Get-AzStorageFileHandle** wyświetla listę uchwytów pliku udziału plików, katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="9e3d8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e3d8-111">EXAMPLES</span></span>

### <span data-ttu-id="9e3d8-112">Przykład 1. Cykliczna lista wszystkich uchwytów plików w udziału plików oraz sortowanie według clientIp i OpenTime</span><span class="sxs-lookup"><span data-stu-id="9e3d8-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="9e3d8-113">To polecenie zawiera listę uchwytów pliku udziału plików i sortowanie danych wyjściowych według clientIp, a następnie według programu OpenTime.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="9e3d8-114">Przykład 2. Cykliczna lista 2 uchwytów pliku w katalogu plików</span><span class="sxs-lookup"><span data-stu-id="9e3d8-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="9e3d8-115">To polecenie wyświetla 2 pierwsze uchwyty pliku w katalogu plików cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="9e3d8-116">Przykład 3. Lista od 3. do 6. uchwytów pliku</span><span class="sxs-lookup"><span data-stu-id="9e3d8-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="9e3d8-117">To polecenie wyświetla od 3. do 6. uchwytów pliku.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="9e3d8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e3d8-118">PARAMETERS</span></span>

### <span data-ttu-id="9e3d8-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e3d8-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9e3d8-120">Maksymalny czas wykonywania po stronie klienta dla każdego żądania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="9e3d8-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9e3d8-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9e3d8-122">Całkowita ilość jednoczesnych zadań synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="9e3d8-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-123">The default value is 10.</span></span>

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

### <span data-ttu-id="9e3d8-124">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9e3d8-124">-Context</span></span>
<span data-ttu-id="9e3d8-125">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9e3d8-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="9e3d8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3d8-126">-DefaultProfile</span></span>
<span data-ttu-id="9e3d8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3d8-128">— Katalog</span><span class="sxs-lookup"><span data-stu-id="9e3d8-128">-Directory</span></span>
<span data-ttu-id="9e3d8-129">Obiekt CloudFileDirectory wskazywał folder bazowy, w którym będą wyświetlane pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="9e3d8-130">— Plik</span><span class="sxs-lookup"><span data-stu-id="9e3d8-130">-File</span></span>
<span data-ttu-id="9e3d8-131">Obiekt CloudFile wskazywał plik na listę uchwytów pliku.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-131">CloudFile object indicated the file to list File Handles.</span></span>

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

### <span data-ttu-id="9e3d8-132">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="9e3d8-132">-Path</span></span>
<span data-ttu-id="9e3d8-133">Ścieżka do istniejącego pliku/katalogu.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d8-134">- Rekurencyjna</span><span class="sxs-lookup"><span data-stu-id="9e3d8-134">-Recursive</span></span>
<span data-ttu-id="9e3d8-135">Uchwyty listy rekurencyjnie.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-135">List handles Recursively.</span></span>
<span data-ttu-id="9e3d8-136">Działa tylko w katalogu plików.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="9e3d8-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e3d8-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9e3d8-138">Czas poszczególnych żądań w sekundach dla serwera jest uy czasowy.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="9e3d8-139">— Udostępnianie</span><span class="sxs-lookup"><span data-stu-id="9e3d8-139">-Share</span></span>
<span data-ttu-id="9e3d8-140">Obiekt CloudFileShare wskazywał udział, w którym będą wyświetlane pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="9e3d8-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9e3d8-141">-ShareName</span></span>
<span data-ttu-id="9e3d8-142">Nazwa udziału plików, w którym będą wyświetlane pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="9e3d8-143">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="9e3d8-143">-IncludeTotalCount</span></span>
<span data-ttu-id="9e3d8-144">Raportuje liczbę obiektów w zestawie danych (liczbę całkowitą), a po niej obiekty.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="9e3d8-145">Jeśli polecenie cmdlet nie może ustalić łącznej liczby, zwraca wartość "Nieznana liczba sum".</span><span class="sxs-lookup"><span data-stu-id="9e3d8-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="9e3d8-146">Obecnie ten parametr nie działa nic.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="9e3d8-147">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="9e3d8-147">-Skip</span></span>
<span data-ttu-id="9e3d8-148">Ignoruje pierwsze "n" obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d8-149">— Najpierw</span><span class="sxs-lookup"><span data-stu-id="9e3d8-149">-First</span></span>
<span data-ttu-id="9e3d8-150">Pobiera tylko pierwsze obiekty "n".</span><span class="sxs-lookup"><span data-stu-id="9e3d8-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3d8-151">CommonParameters</span></span>
<span data-ttu-id="9e3d8-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3d8-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3d8-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3d8-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e3d8-154">INPUTS</span></span>

### <span data-ttu-id="9e3d8-155">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9e3d8-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9e3d8-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9e3d8-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9e3d8-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e3d8-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e3d8-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e3d8-158">OUTPUTS</span></span>

### <span data-ttu-id="9e3d8-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="9e3d8-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="9e3d8-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e3d8-160">NOTES</span></span>

## <span data-ttu-id="9e3d8-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e3d8-161">RELATED LINKS</span></span>
