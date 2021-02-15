---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190899"
---
# <span data-ttu-id="3954c-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3954c-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="3954c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3954c-102">SYNOPSIS</span></span>
<span data-ttu-id="3954c-103">Wyświetla listę obiektów blob w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="3954c-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="3954c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3954c-104">SYNTAX</span></span>

### <span data-ttu-id="3954c-105">BlobName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3954c-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3954c-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="3954c-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3954c-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="3954c-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3954c-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="3954c-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3954c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3954c-109">DESCRIPTION</span></span>
<span data-ttu-id="3954c-110">Polecenie **cmdlet Get-AzStorageBlob** wyświetla listę obiektów blob w określonym kontenerze na koncie magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3954c-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="3954c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3954c-111">EXAMPLES</span></span>

### <span data-ttu-id="3954c-112">Przykład 1. Uzyskiwanie obiektu blob według nazwy obiektu blob</span><span class="sxs-lookup"><span data-stu-id="3954c-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="3954c-113">To polecenie używa nazwy obiektu blob i symbolu wieloznacznego w celu uzyskania obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="3954c-114">Przykład 2. Uzyskiwanie obiektów blob w kontenerze przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="3954c-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="3954c-115">To polecenie używa potoku w celu uzyskania wszystkich obiektów blob (w tym obiektów blob w stanie Usunięte) w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="3954c-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="3954c-116">Przykład 3. Uzyskiwanie obiektów blob według prefiksu nazwy</span><span class="sxs-lookup"><span data-stu-id="3954c-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="3954c-117">To polecenie używa prefiksu nazwy do uzyskania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="3954c-118">Przykład 4. Lista obiektów blob w wielu partiach</span><span class="sxs-lookup"><span data-stu-id="3954c-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="3954c-119">W tym przykładzie parametry *MaxCount* i *ContinuationToken* są używane do listy obiektów blob magazynu platformy Azure w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="3954c-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="3954c-120">Pierwsze cztery polecenia przypiszą wartości do zmiennych, których będzie można użyć w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="3954c-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="3954c-121">Piąte polecenie określa instrukcji **Do-While,** która używa polecenia cmdlet **Get-AzStorageBlob** w celu uzyskania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="3954c-122">Instrukcja zawiera token kontynuacji przechowywany w $Token zmiennej.</span><span class="sxs-lookup"><span data-stu-id="3954c-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="3954c-123">$Token zmienia wartość w pętli.</span><span class="sxs-lookup"><span data-stu-id="3954c-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="3954c-124">Aby uzyskać więcej informacji, wpisz `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="3954c-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="3954c-125">Ostatnie polecenie wyświetla sumę **za** pomocą polecenia Echo.</span><span class="sxs-lookup"><span data-stu-id="3954c-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="3954c-126">Przykład 5. Pobierz wszystkie obiekty blob w kontenerze zawierają wersję obiektów blob</span><span class="sxs-lookup"><span data-stu-id="3954c-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="3954c-127">To polecenie pobiera wszystkie obiekty blob w kontenerze, w tym wersję obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="3954c-128">Przykład 6. Uzyskiwanie wersji pojedynczego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="3954c-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="3954c-129">To polecenie pobiera pojedynczy obiekt blob z polem VersionId.</span><span class="sxs-lookup"><span data-stu-id="3954c-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="3954c-130">Przykład 7. Uzyskiwanie migawki pojedynczego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="3954c-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="3954c-131">To polecenie pobiera migawkę pojedynczego obiektu blob z migawką MigawkaGodziny.</span><span class="sxs-lookup"><span data-stu-id="3954c-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="3954c-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3954c-132">PARAMETERS</span></span>

### <span data-ttu-id="3954c-133">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="3954c-133">-Blob</span></span>
<span data-ttu-id="3954c-134">Określa nazwę lub deseń nazw, których można używać do wyszukiwania z symbolami wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="3954c-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="3954c-135">Jeśli nie określono nazwy obiektu blob, polecenie cmdlet wyświetla listę wszystkich obiektów blob w określonym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="3954c-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="3954c-136">Jeśli dla tego parametru zostanie określona wartość, polecenie cmdlet wyświetla listę wszystkich obiektów blob o nazwach, które pasują do tego parametru.</span><span class="sxs-lookup"><span data-stu-id="3954c-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="3954c-137">Ten parametr obsługuje symbole wieloznaczne w dowolnym miejscu ciągu.</span><span class="sxs-lookup"><span data-stu-id="3954c-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3954c-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3954c-139">Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="3954c-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3954c-140">Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.</span><span class="sxs-lookup"><span data-stu-id="3954c-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3954c-141">Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="3954c-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3954c-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3954c-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3954c-143">Określa maksymalną jednoczesną liczbę połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3954c-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3954c-144">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="3954c-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3954c-145">Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.</span><span class="sxs-lookup"><span data-stu-id="3954c-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3954c-146">Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="3954c-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3954c-147">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="3954c-147">The default value is 10.</span></span>

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

### <span data-ttu-id="3954c-148">— Kontener</span><span class="sxs-lookup"><span data-stu-id="3954c-148">-Container</span></span>
<span data-ttu-id="3954c-149">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="3954c-149">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-150">— kontekst</span><span class="sxs-lookup"><span data-stu-id="3954c-150">-Context</span></span>
<span data-ttu-id="3954c-151">Określa konto magazynu platformy Azure, z którego chcesz uzyskać listę obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="3954c-152">Możesz użyć polecenia cmdlet New-AzStorageContext, aby utworzyć kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="3954c-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="3954c-153">-ContinuationToken</span></span>
<span data-ttu-id="3954c-154">Określa token kontynuacji dla listy obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="3954c-155">Użyj tego parametru i *parametru MaxCount,* aby wyświetlić listę obiektów blob w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="3954c-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3954c-156">-DefaultProfile</span></span>
<span data-ttu-id="3954c-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3954c-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3954c-158">- IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="3954c-158">-IncludeDeleted</span></span>
<span data-ttu-id="3954c-159">Dołącz usunięty obiekt blob, domyślnie obiekt blob get nie będzie uwzględniał usuniętego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="3954c-160">- IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="3954c-160">-IncludeVersion</span></span>
<span data-ttu-id="3954c-161">Wersje obiektów blob będą wyświetlane tylko wtedy, gdy ten parametr istnieje, domyślnie get blob nie będzie zawierał wersji obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3954c-162">-MaxCount</span></span>
<span data-ttu-id="3954c-163">Określa maksymalną liczbę obiektów zwracanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3954c-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="3954c-164">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="3954c-164">-Prefix</span></span>
<span data-ttu-id="3954c-165">Określa prefiks dla nazw obiektów blob, które mają zostać uzyskać.</span><span class="sxs-lookup"><span data-stu-id="3954c-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="3954c-166">Ten parametr nie obsługuje wyszukiwania przy użyciu wyrażeń regularnych ani symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="3954c-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="3954c-167">Oznacza to, że jeśli kontener zawiera tylko obiekty blob o nazwach "My", "MyBlob1" i "MyBlob2" i określisz "-Prefix My\*", polecenie cmdlet nie zwróci żadnych obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="3954c-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="3954c-168">Jeśli jednak określisz "-Prefix My", polecenie cmdlet zwróci wartości "My", "MyBlob1" i "MyBlob2".</span><span class="sxs-lookup"><span data-stu-id="3954c-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3954c-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3954c-170">Określa interwał po stronie usługi (w sekundach) dla żądania.</span><span class="sxs-lookup"><span data-stu-id="3954c-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3954c-171">Jeśli po upływie określonego interwału usługa przetwarza żądanie, usługa magazynu zwraca błąd.</span><span class="sxs-lookup"><span data-stu-id="3954c-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3954c-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="3954c-172">-SnapshotTime</span></span>
<span data-ttu-id="3954c-173">Migawka obiektów blob</span><span class="sxs-lookup"><span data-stu-id="3954c-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="3954c-174">-VersionId</span></span>
<span data-ttu-id="3954c-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="3954c-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3954c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3954c-176">CommonParameters</span></span>
<span data-ttu-id="3954c-177">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3954c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3954c-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3954c-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3954c-179">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3954c-179">INPUTS</span></span>

### <span data-ttu-id="3954c-180">System.String</span><span class="sxs-lookup"><span data-stu-id="3954c-180">System.String</span></span>

### <span data-ttu-id="3954c-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3954c-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3954c-182">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3954c-182">OUTPUTS</span></span>

### <span data-ttu-id="3954c-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3954c-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="3954c-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3954c-184">NOTES</span></span>

## <span data-ttu-id="3954c-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3954c-185">RELATED LINKS</span></span>

[<span data-ttu-id="3954c-186">Get-AzstorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3954c-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="3954c-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3954c-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="3954c-188">Set-AzstorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3954c-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


