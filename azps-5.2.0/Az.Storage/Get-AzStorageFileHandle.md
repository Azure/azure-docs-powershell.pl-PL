---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349630"
---
# <span data-ttu-id="3f3a6-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3f3a6-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="3f3a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3a6-103">Zawiera listę dojść do plików udziału plików, katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="3f3a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f3a6-104">SYNTAX</span></span>

### <span data-ttu-id="3f3a6-105">Nazwa_udziału (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3f3a6-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3f3a6-106">Udostępnij</span><span class="sxs-lookup"><span data-stu-id="3f3a6-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3f3a6-107">Directory</span><span class="sxs-lookup"><span data-stu-id="3f3a6-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3f3a6-108">Plik</span><span class="sxs-lookup"><span data-stu-id="3f3a6-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="3f3a6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3f3a6-109">DESCRIPTION</span></span>
<span data-ttu-id="3f3a6-110">Polecenie cmdlet **Get-AzStorageFileHandle** zawiera listę dojść do plików udziału plików lub katalogu plików lub pliku.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="3f3a6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f3a6-111">EXAMPLES</span></span>

### <span data-ttu-id="3f3a6-112">Przykład 1: pocyklicznie Wyświetl wszystkie uchwyty plików w udziale plików, a następnie Sortuj według ClientIp i OpenTime</span><span class="sxs-lookup"><span data-stu-id="3f3a6-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
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

<span data-ttu-id="3f3a6-113">To polecenie wyświetla listę dojść do plików w udziale plików i sortuje dane wyjściowe według ClientIp, a następnie OpenTime.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="3f3a6-114">Przykład 2: Lista pierwszych 2 dojść do plików w katalogu plików rekurencyjnie</span><span class="sxs-lookup"><span data-stu-id="3f3a6-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="3f3a6-115">To polecenie wyświetla cyklicznie listę pierwszych 2 dojść do plików w katalogu plików.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="3f3a6-116">Przykład 3: Wyświetlanie listy od trzeciej do szóstego uchwytu do pliku</span><span class="sxs-lookup"><span data-stu-id="3f3a6-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="3f3a6-117">To polecenie wyświetla listę od trzeciego do szóstego dojścia do pliku w pliku.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="3f3a6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f3a6-118">PARAMETERS</span></span>

### <span data-ttu-id="3f3a6-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f3a6-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3f3a6-120">Maksymalny czas wykonywania wszystkich żądań po stronie klienta (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="3f3a6-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="3f3a6-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3f3a6-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3f3a6-122">Całkowita liczba współbieżnych zadań asynchronicznych.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="3f3a6-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-123">The default value is 10.</span></span>

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

### <span data-ttu-id="3f3a6-124">-Context</span><span class="sxs-lookup"><span data-stu-id="3f3a6-124">-Context</span></span>
<span data-ttu-id="3f3a6-125">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="3f3a6-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="3f3a6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3a6-126">-DefaultProfile</span></span>
<span data-ttu-id="3f3a6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f3a6-128">-Directory</span><span class="sxs-lookup"><span data-stu-id="3f3a6-128">-Directory</span></span>
<span data-ttu-id="3f3a6-129">Obiekt CloudFileDirectory wskazuje podstawowy folder, w którym znajdują się pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="3f3a6-130">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="3f3a6-130">-File</span></span>
<span data-ttu-id="3f3a6-131">Obiekt CloudFile wskazał na plik listę dojść do pliku.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-131">CloudFile object indicated the file to list File Handles.</span></span>

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

### <span data-ttu-id="3f3a6-132">-Path</span><span class="sxs-lookup"><span data-stu-id="3f3a6-132">-Path</span></span>
<span data-ttu-id="3f3a6-133">Ścieżka do istniejącego pliku/katalogu.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-133">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="3f3a6-134">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="3f3a6-134">-Recursive</span></span>
<span data-ttu-id="3f3a6-135">Lista dojść rekurencyjnych.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-135">List handles Recursively.</span></span>
<span data-ttu-id="3f3a6-136">Działa tylko w katalogu plików.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="3f3a6-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f3a6-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3f3a6-138">Upłynął limit czasu serwera dla każdego żądania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="3f3a6-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="3f3a6-139">-Share</span><span class="sxs-lookup"><span data-stu-id="3f3a6-139">-Share</span></span>
<span data-ttu-id="3f3a6-140">Obiekt CloudFileShare wskazuje udział, w którym znajdują się listy plików/katalogów.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="3f3a6-141">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="3f3a6-141">-ShareName</span></span>
<span data-ttu-id="3f3a6-142">Nazwa udziału plików, w którym będą wyświetlane pliki/katalogi.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="3f3a6-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="3f3a6-143">-IncludeTotalCount</span></span>
<span data-ttu-id="3f3a6-144">Wyświetla liczbę obiektów w zbiorze danych (liczba całkowita), a następnie obiekty.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="3f3a6-145">Jeśli polecenie cmdlet nie może ustalić całkowitej liczby, zwraca wartość "Łączna liczba nieznanych".</span><span class="sxs-lookup"><span data-stu-id="3f3a6-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="3f3a6-146">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="3f3a6-147">-Skip</span><span class="sxs-lookup"><span data-stu-id="3f3a6-147">-Skip</span></span>
<span data-ttu-id="3f3a6-148">Ignoruje pierwsze obiekty ' n ', a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="3f3a6-149">-First</span><span class="sxs-lookup"><span data-stu-id="3f3a6-149">-First</span></span>
<span data-ttu-id="3f3a6-150">Pobiera tylko pierwsze obiekty "n".</span><span class="sxs-lookup"><span data-stu-id="3f3a6-150">Gets only the first 'n' objects.</span></span>

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

### <span data-ttu-id="3f3a6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3a6-151">CommonParameters</span></span>
<span data-ttu-id="3f3a6-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f3a6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3a6-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f3a6-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3a6-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f3a6-154">INPUTS</span></span>

### <span data-ttu-id="3f3a6-155">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3f3a6-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="3f3a6-156">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3f3a6-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="3f3a6-157">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f3a6-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3f3a6-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f3a6-158">OUTPUTS</span></span>

### <span data-ttu-id="3f3a6-159">Microsoft. Azure. Storage. File. FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="3f3a6-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="3f3a6-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f3a6-160">NOTES</span></span>

## <span data-ttu-id="3f3a6-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f3a6-161">RELATED LINKS</span></span>
